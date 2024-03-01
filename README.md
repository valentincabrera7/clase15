# pdw en la terminal para saber donde estoy parado en powershell
# mkdir para crear una carpeta (mkdir y el nombre de la carpeta en la terminal)
# cd para situarme en el directorio de la carpeta que haya creado (para acceder)

from datetime import date, datetime, time

class Persona:
    def __init__(self, nombre, apellido, nacimimiento: datetime) -> None:
        self.nombre = nombre 
        self.apellido = apellido
        self.nacimiento = nacimimiento

    def nacimiento_f(self): # cuando llamo al self, llamo a este metodo para que ejecuta strftime del atributo nacimiento
        return self.nacimiento.strftime(r"%d/%m/%y")

    def __str__(self) -> str:
        return f"{self.nombre}, {self.apellido}. Nacio el {self.nacimiento_f()}"

#nacimiento = input("Fecha de nacimiento: ")
#fecha_nacimiento = datetime.strptime(nacimiento, r"%d/%m/%yY")

p1 = Persona("Valentin", "Cabrera", datetime(1998, 4, 11)) 
print(p1)

#import locale # para importar
#locale.setlocale(locale.LC_ALL, "") # para que me diga que dia de la semana es
#print(f"Hoy es {datetime.today().strftime('%D')}")



