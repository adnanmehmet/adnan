# adnan
adnan mehmet
using System;
using System.Windows.Forms;

namespace WindowsFormsUygulamasi
{
    public class MyForm : Form
    {
        private Button button;
        private Label label;

        public MyForm()
        {
            this.Text = "Windows Forms Uygulaması";
            this.Size = new System.Drawing.Size(300, 200);

            label = new Label();
            label.Text = "Merhaba Dünya!";
            label.Location = new System.Drawing.Point(50, 50);
            label.AutoSize = true;

            button = new Button();
            button.Text = "Tıkla";
            button.Location = new System.Drawing.Point(100, 100);
            button.Click += Button_Click;

            this.Controls.Add(label);
            this.Controls.Add(button);
        }

        private void Button_Click(object sender, EventArgs e)
        {
            label.Text = "Butona tıklandı!";
        }
    }

    public class Program
    {
        [STAThread]
        public static void Main()
        {
            Application.Run(new MyForm());
        }
    }
}
