# CyrillicShift
Library for text translation in CyrillicShift

## 🚨 Important Note: Case Sensitivity

The current version (0.1.1) only supports **lowercase letters**. 
Capital letters will not be converted correctly.

**Workaround:**
```csharp
// Convert to lowercase before processing
var result = CyrillicShiftConverter.EncodeToCyrillic(myString.ToLower());
```

# Example Code:
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
            Console.WriteLine(Word); // hвllд ыдаld
            Word = CyrillicShiftClass.DecodeToLatin(Word);
            Console.WriteLine(Word); // hellogworld
        }
    }
}
```
