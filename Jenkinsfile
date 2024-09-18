import java.text.SimpleDateFormat
def fecha_nac = 2001
def fecha_actual = new Date()
def nombre_fichero = "edad_calculada.txt"
def ruta_del_fichero = "C:\\Users\\jcampom\\Desktop\\"
def edad = 0
pipeline
{
    agent any
    stages
    {
        stage("edad")
        {
            steps
            {
              script{
              def anio_actual = fecha_actual.getYear() 
              edad = anio_actual - fecha_nac
              }
            }   
        }
        stage ("fichero"){
          steps
              {
                script{
                    texto = "La edad es: ${edad}" 
                    fichero = ruta_del_fichero + nombre_fichero
                    writeFile(file: fichero, text: texto)
                    echo "Archivo creado con la edad calculada en: ${fichero}"
                  
                }
              }   
        }
    }
}
