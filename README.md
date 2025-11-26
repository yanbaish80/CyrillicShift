# CyrillicShift Converter

A lightweight .NET library for converting text between Latin and Cyrillic keyboard layouts. Perfect for fixing the "wrong layout" typing problem.

## ⚠️ WARNING: Experimental Version

The current version (0.1.1) has a lot of bugs, so many answers may be incorrect!
Use only for testing and development purposes. We'll fix this soon.

## 🚨 Important Note: Case Sensitivity

🚨 The current version (0.1.1) only supports **lowercase letters**. 
Capital letters will not be converted correctly.

**Workaround:**
```csharp
// Convert to lowercase before processing
var result = CyrillicShiftConverter.EncodeToCyrillic(myString.ToLower());
```

### **🔮 For future versions can be fixed:**
```csharp
// Planned for v1.1.0:
public static string EncodeToCyrillic(string input, bool preserveCase = false)
{
    // Implementation with case support
}
```

## 🔮 Future Plans
🔮 v1.1.0: Add uppercase letter support

🔮 v1.2.0: Add case preservation option

🔮 v2.0.0: Add additional keyboard layouts

## 🚨 Current Limitations
🚨 Only lowercase letters are supported

🚨 Inaccurate character mappings in some cases

🚨 Mixed case input will produce unexpected results

🚨 Limited symbol coverage


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
            string Word = CyrillicShiftConverter.EncodeToCyrillic("hello world");
            Console.WriteLine(Word); // рвddф ьфsыв
            Word = CyrillicShiftConverter.DecodeToLatin(Word);
            Console.WriteLine(Word); // hello world
            // The current version (0.1.1) has a lot of bugs, so many answers may be incorrect.
        }
    }
}
```
