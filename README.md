# CyrillicShift
Library for text translation in CyrillicShift

Example Code:
```
using System;
using System.Windows.Forms;
using CyrillicShift;

namespace TestLibCyrillicShift
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            string Word = CyrillicShiftClass.EncodeToCyrillic("hello world");
            Console.WriteLine(Word); //Console hвllд ыдаld
        }
    }
}

```
