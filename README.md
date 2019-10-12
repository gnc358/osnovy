using System;
using System.Windows.Forms;

namespace Laba3
{
    public partial class Form2 : Form
    {
        public Form2()	
        {	
            InitializeComponent();
        }
        double Vvod(TextBox t)
        {
            return Convert.ToDouble(t.Text);
        }
        void Vivod(TextBox t, double z)
        {
            t.Text = z.ToString("F5");
        }
        class Class1
        {
            public static double Duga1(double r1, double a)
            {
                double dl = 2 * Math.PI * r1 * (a / 360);
                return dl;
            }
        }
        private void Button1_Click(object sender, EventArgs e)
        {
            double r1, r2, r3, a, b, c;
            r1 = Vvod(textBox1);
            r2 = Vvod(textBox3);
            r3 = Vvod(textBox5);
            a = Vvod(textBox2);
            b = Vvod(textBox4);
            c = Vvod(textBox6);
            double l1 = Class1.Duga1(r1, a);
            double l2 = Class1.Duga1(r2, b);
            double l3 = Class1.Duga1(r3, c);
            Vivod(textBox7, l1);
            Vivod(textBox8, l2);
            Vivod(textBox9, l3);
        }
        
        
    }
}
