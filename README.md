# Entity Framework Core - Mappings

Para ejecutar el codigo sera necesario crear la base de datos, lo cual se realiza por medio de migrations

![enter image description here](https://raw.githubusercontent.com/ltuttini/EntityFrameworkCoreMappings/master/media/UpdateDb.jpg)

> Importante: Notar los 3 puntos resaltados en amarillo.

El connection string lo obtienes del contexto, es alli donde migrations creara la Db

    protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
	{
		optionsBuilder
			.UseLoggerFactory(MyConsoleLoggerFactory)
			.UseSqlServer("Server = (local); Database = UniversityData; Trusted_Connection = True; ")
			.EnableSensitiveDataLogging(true);
	}

Si el servicio de sql server esta en un server diferente, deberan cambiarlo

Una vez que la Db este creada cambiar el startup project a **ConsoleUI**, para asi habilitar los test.


