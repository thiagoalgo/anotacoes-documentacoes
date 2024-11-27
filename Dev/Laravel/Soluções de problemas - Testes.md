## Livewire - testar campos JSON no banco de dados

```php
public function test_save()  
{  
    $this->login('job-openings-manage', 'Admin');  
  
    Department::factory(5)->create();  
    JobTitle::factory(5)->create();  
    BusinessUnit::factory(5)->create();  
    Employee::factory(5)->create();  
    Role::create(['name' => 'Colaborador']);  
  
    $jobOpening = JobOpening::factory()->create();  
  
    Livewire::test(JobOpeningEdit::class, ['jobOpening' => $jobOpening])  
        ->set('form.name', 'Job Opening 2')  
        ->set('form.roles', [2])   // <==========================
        ->call('save');  
  
    $this->assertDatabaseHas('job_openings', [  
        'name' => 'Job Opening 2',  
        'roles' => $this->castAsJson([2]),   // <==========================
    ]);
    ```

## TenantCouldNotBeIdentifiedOnDomainException

Verificar se tem a propriedade abaixo na classe de teste:

```php
protected $tenancy = true;
```

Caso já tenha, pode ser usado o comando abaixo que limpa o cache de autoload, entre outras coisas:

```bash
composer install
```

