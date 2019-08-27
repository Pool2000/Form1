# Form1
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Universidad1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void textBox3_TextChanged(object sender, EventArgs e)
        {

        }
        static Alumno Alumno = new Alumno();
        private void btnRegistrar_Click(object sender, EventArgs e)
        {
            string codigo, apellidos, nombres;
            int edad;
            codigo = txtCodigo.Text;
            apellidos = txtApellidos.Text;
            nombres = txtNombres.Text;
            edad = int.Parse(txtEdad.Text);

           Alumno.Codigo = codigo;
           Alumno.Nombres = nombres;
           Alumno.Apellidos = apellidos;
           Alumno.Edad = edad;
            MessageBox.Show("se registro correctamente");
            txtCodigo.Text="" ;
            txtApellidos.Text="" ;
            txtNombres.Text="" ;
            txtEdad.Text="" ;
            txtCodigo.Focus();


        }

        private void btnMostrar_Click(object sender, EventArgs e)
        {
            string codigo = Alumno.Codigo;
            string apellidos = Alumno.Apellidos;
            string nombres = Alumno.Nombres;
            string edad = Alumno.Edad.ToString();
            MessageBox.Show("codigo: " + codigo + " apellidos: " + apellidos + "nombres: " + nombres + " edad: " + edad );

        }

        private void btnEstudiar_Click(object sender, EventArgs e)
        {
            //mostrar el metodo estudiar
            MessageBox.Show(Alumno.Estudiar());
        }

        private void btnHacerTarea_Click(object sender, EventArgs e)
        {
            //mostrar el metodo hacer atrea
            MessageBox.Show(Alumno.HacerTareas());

        }

        private void btnAsistir_Click(object sender, EventArgs e)
        {
            //mostrar el metodo asistir
            MessageBox.Show(Alumno.Asistir());
        }
        
    }
}
