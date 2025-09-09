# GitHub Copilot 指南 - C# 初學者

## 🎯 專案概述

這是一個專為 C# 初學者設計的學習專案。本專案包含多個練習，幫助您掌握 C# 程式設計的基礎概念。

## 🚀 開發環境設定

- **開發環境**: Visual Studio Code 或 Visual Studio
- **程式語言**: C#
- **框架版本**: .NET 8.0
- **專案類型**: 控制台應用程式 (Console Application)

## 📚 學習目標

1. 熟悉 C# 基本語法
2. 理解物件導向程式設計概念
3. 學會使用 .NET 核心類別庫
4. 掌握除錯和測試技巧

## 💡 GitHub Copilot 使用指南

### 程式碼產生建議

當您需要 Copilot 幫助時，請使用清楚的中文或英文註解描述您的需求：

```csharp
// 建立一個方法來計算兩個數字的總和
// Create a method to calculate the sum of two numbers

// 使用迴圈列印乘法表
// Use a loop to print multiplication table

// 驗證使用者輸入是否為有效數字
// Validate if user input is a valid number
```

### 最佳實務範例

#### 1. 變數命名 (Variable Naming)

```csharp
// 好的命名方式 ✅
int studentAge = 18;
string userName = "張三";
bool isValidInput = true;

// 避免的命名方式 ❌
int a = 18;
string s = "張三";
bool flag = true;
```

#### 2. 方法設計 (Method Design)

```csharp
// 清楚的方法簽名和用途
public static int CalculateSum(int firstNumber, int secondNumber)
{
    return firstNumber + secondNumber;
}

// 包含輸入驗證
public static bool IsValidNumber(string input)
{
    return int.TryParse(input, out _);
}
```

#### 3. 錯誤處理 (Error Handling)

```csharp
try
{
    // 可能發生例外的程式碼
    int number = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine($"您輸入的數字是: {number}");
}
catch (FormatException)
{
    Console.WriteLine("錯誤：請輸入有效的數字");
}
catch (Exception ex)
{
    Console.WriteLine($"發生未預期的錯誤: {ex.Message}");
}
```

## 🔧 常用程式碼片段

### 使用者輸入處理

```csharp
// 提示：請為我建立一個安全的數字輸入方法
// Prompt: Please create a safe number input method for me
```

### 迴圈結構

```csharp
// 提示：建立一個 for 迴圈來列印 1 到 10
// Prompt: Create a for loop to print numbers from 1 to 10
```

### 條件判斷

```csharp
// 提示：檢查數字是否為偶數
// Prompt: Check if a number is even
```

## 📝 專案結構說明

### Day01FirstConsoleApp

- **目的**: 熟悉 C# 基本語法和控制台輸出
- **重點**: `Console.WriteLine()`, 變數宣告, 基本資料型別

### Day01MultiplicationTable

- **目的**: 學習迴圈和數學運算
- **重點**: `for` 迴圈, 格式化輸出, 數學計算

## 🎨 程式碼風格指南

### 1. 縮排和格式化

- 使用 4 個空格作為縮排
- 大括號 `{` `}` 各占一行
- 運算子前後加空格

### 2. 註解撰寫

```csharp
/// <summary>
/// 計算兩個整數的乘積
/// Calculates the product of two integers
/// </summary>
/// <param name="a">第一個數字</param>
/// <param name="b">第二個數字</param>
/// <returns>兩數的乘積</returns>
public static int Multiply(int a, int b)
{
    return a * b;
}
```

## 🐛 除錯技巧

### 1. 使用 Console.WriteLine 除錯

```csharp
// 在關鍵位置加入除錯輸出
Console.WriteLine($"Debug: 變數 x 的值為 {x}");
```

### 2. 使用中斷點 (Breakpoints)

- 在程式碼行號左側點擊設定中斷點
- 使用 F5 開始除錯模式
- 使用 F10 逐行執行

## 💬 與 Copilot 對話範例

### 要求程式碼解釋

```
// 請解釋這段程式碼的作用
// Please explain what this code does
for (int i = 1; i <= 10; i++)
{
    for (int j = 1; j <= 10; j++)
    {
        Console.Write($"{i * j:D3} ");
    }
    Console.WriteLine();
}
```

### 要求程式碼優化

```
// 請幫我優化這個方法，使其更有效率
// Please help me optimize this method to make it more efficient
```

### 要求錯誤修正

```
// 這段程式碼有什麼問題？請幫我修正
// What's wrong with this code? Please help me fix it
```

## 🎓 學習進度建議

### 第一週：基礎概念

- [ ] 變數和資料型別
- [ ] 基本輸入輸出
- [ ] 條件判斷 (if-else)
- [ ] 迴圈 (for, while)

### 第二週：進階概念

- [ ] 陣列和集合
- [ ] 方法定義和呼叫
- [ ] 例外處理
- [ ] 字串操作

### 第三週：物件導向

- [ ] 類別和物件
- [ ] 封裝、繼承、多型
- [ ] 介面和抽象類別

## 🚨 常見錯誤和解決方案

### 1. 編譯錯誤

```
錯誤 CS0103: 名稱 'variableName' 不存在於目前內容中
解決方案: 檢查變數名稱拼寫和宣告位置
```

### 2. 執行時期錯誤

```
System.FormatException: 輸入字串的格式不正確
解決方案: 使用 TryParse 方法進行安全轉換
```

## 📞 尋求協助

當您遇到問題時，可以：

1. 詢問 Copilot: "這個錯誤是什麼意思？" 或 "What does this error mean?"
2. 要求範例: "請給我一個 XXX 的範例" 或 "Please give me an example of XXX"
3. 請求解釋: "請解釋這個概念" 或 "Please explain this concept"

記住，學習程式設計是一個循序漸進的過程。不要害怕犯錯，每個錯誤都是學習的機會！

---

_此指南將隨著學習進度持續更新。祝您學習愉快！_ 🎉
