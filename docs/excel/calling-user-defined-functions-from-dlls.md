---
title: Dll からユーザー定義関数の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], calling from dlls,user-defined functions [Excel 2007], calling from DLLs,DLLs [Excel 2007], calling UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798776"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="7c304-104">Dll からユーザー定義関数の呼び出し</span><span class="sxs-lookup"><span data-stu-id="7c304-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="7c304-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7c304-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7c304-p101">���[�N�V�[�g����̃��[�U�[��[](xludf.md)�ς݊֐��R�[�h�͂���܂���BUDF ��Ăяo����悤�ɁAC API �� XLL ��p�̊֐��A�܂� [xlUDF ](xludf.md) �֐���G�N�X�|�[�g���܂��B�֐��̍ŏ��̈����́A�֐����ł��镶����ŁA�㑱�̈����� UDF ���ʏ�z�肵�Ă��镶����ł��B</span><span class="sxs-lookup"><span data-stu-id="7c304-p101">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula. However, from the C API, there are no pre-defined function codes to use with the call-backs. To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function. The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="7c304-p102">���� 44 ��w�肵�� **xlfGetWorkspace** �֐���g�p���āA���ݓo�^����Ă��� XLL �A�h�C���̊֐��ƃR�}���h�̈ꗗ��擾�ł��܂��B����� 3 ��̔z���Ԃ��A�e��͎���\���܂��B</span><span class="sxs-lookup"><span data-stu-id="7c304-p102">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44. This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="7c304-112">XLL �̊��S�p�X�ƃt�@�C����</span><span class="sxs-lookup"><span data-stu-id="7c304-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="7c304-113">XLL ����G�N�X�|�[�g���ꂽ UDF �܂��̓R�}���h�̖��O</span><span class="sxs-lookup"><span data-stu-id="7c304-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="7c304-114">�߂�l�ƈ����R�[�h������</span><span class="sxs-lookup"><span data-stu-id="7c304-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="7c304-115">XLL �t�@�C������G�N�X�|�[�g���ꂽ�Ƃ��̖��O�́AExcel ���F�����Ă��� UDF �܂��̓R�}���h�̓o�^���Ƃ͈�v���Ȃ��\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="7c304-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="7c304-p103">Excel 2007 �ȍ~�́A���̓c�[�� (ATP) �֐��͊��S�ɑg�ݍ��܂�Ă���AC API �ɂ́APRICE �� **xlfPrice** �Ȃǂ̊֐��ɑ΂��邻�̓Ǝ��̗񋓑̂�����܂��B�ȑO�̃o�[�W�����ł́A���������֐��̎g�p�ɂ́A **xlUDF** ��g�p����K�v������܂����B�A�h�C���� Excel 2003 ����� Excel 2007 �ȍ~�̃o�[�W�����Ŏg���K�v������A�A�h�C�������������֐���g���ꍇ�A���[�U�[���ŐV�o�[�W��������肵�āA�K�؂ȕ��@�Ŋ֐���Ăяo���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="7c304-p103">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**. In earlier versions, you had to use **xlUDF** to call these functions. If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="7c304-119">��</span><span class="sxs-lookup"><span data-stu-id="7c304-119">Examples</span></span>

<span data-ttu-id="7c304-p104">���̗�́A���s���� Excel �̃o�[�W������ 2003 �ȑO�̏ꍇ�ɁAATP �֐� **PRICE** ��Ăяo�� **xlUDF** �֐���\���Ă��܂��B�O���[�o�� �o�[�W�����ϐ� (���̗�ł� **gExcelVersion12plus** �Ȃ�) �̐ݒ�ɂ��ẮA [���ʌ݊���](backward-compatibility.md) ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="7c304-p104">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier. For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7c304-122">���̗�ł́A�t���[�����[�N�֐� **TempNum**�A **TempStrConst** ��g�p���A��������� Excel �� C API ��Ăяo���悤�ɐݒ肵�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="7c304-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

<span data-ttu-id="7c304-p105">�C���v���[�X�ň�����ύX���āA�l��Ԃ� XLL �֐���Ăяo���Ă�A **xlUDF** �֐��͂���܂łǂ���A���� **XLOPER/XLOPER12** �̃A�h���X��g�p���Ēl��Ԃ��܂��B�܂�A�ʏ�� return �X�e�[�g�����g��p���邩�̂悤�ɂ��Č��ʂ�Ԃ��܂��B�߂�l�Ɏg�p���������ɑΉ����� **XLOPER/XLOPER12** �͕ύX����Ă��܂���B���Ƃ��΁A���� 2 �� UDF ��l���Ă݂Ă��������B</span><span class="sxs-lookup"><span data-stu-id="7c304-p105">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**. In other words, the result is returned as if through a normal return statement. The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified. For example, consider the following two UDFs.</span></span> 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

<span data-ttu-id="7c304-127">**UDF\_2**の呼び出し**UDF\_1**、 **pxArg**の値変更されず**Excel12**への呼び出しの後、 **xRetVal**の**UDF_1**によって返される値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c304-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="7c304-p106">���̕��@�� UDS �ւ̌Ăяo���񐔂𑽂��s���ꍇ�A�܂��ŏ��� [xlfEvaluate �֐�](xlfevaluate.md)��g�p���Ċ֐��̖��O��]���ł��܂��B���̌��ʂ̐��́A **xlfRegister** �֐����Ԃ��o�^ ID �Ɠ����ŁA�֐����̑���� **xlUDF** �֐��ւ̍ŏ��̈����Ƃ��ēn�����Ƃ��ł��܂��B����ɂ�� Excel �́A�֐����̌���������K�v�ȏꍇ�ɔ�ׁA��葬���֐�������A�Ăяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="7c304-p106">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md). The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function. This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c304-131">�֘A����</span><span class="sxs-lookup"><span data-stu-id="7c304-131">See also</span></span>

- <span data-ttu-id="7c304-132">[���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)</span><span class="sxs-lookup"><span data-stu-id="7c304-132">[Permitting User Breaks in Lengthy Operations](permitting-user-breaks-in-lengthy-operations.md)</span></span>
- [<span data-ttu-id="7c304-133">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="7c304-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="7c304-134">Excel XLL SDK �̊T�v</span><span class="sxs-lookup"><span data-stu-id="7c304-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

