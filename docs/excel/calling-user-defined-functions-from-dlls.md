---
title: DLL からのユーザー定義関数の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], calling from dlls,user-defined functions [Excel 2007], calling from DLLs,DLLs [Excel 2007], calling UDFs
ms.localizationpriority: medium
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 443e111d15365cdc1145e659446a2866f7c0a263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614613"
---
# <a name="calling-user-defined-functions-from-dlls"></a>DLL からのユーザー定義関数の呼び出し

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
���[�N�V�[�g����̃��[�U�[��[](xludf.md)�ς݊֐��R�[�h�͂���܂���BUDF ��Ăяo����悤�ɁAC API �� XLL ��p�̊֐��A�܂� [xlUDF ](xludf.md) �֐���G�N�X�|�[�g���܂��B�֐��̍ŏ��̈����́A�֐����ł��镶����ŁA�㑱�̈����� UDF ���ʏ�z�肵�Ă��镶����ł��B 
  
���� 44 ��w�肵�� **xlfGetWorkspace** �֐���g�p���āA���ݓo�^����Ă��� XLL �A�h�C���̊֐��ƃR�}���h�̈ꗗ��擾�ł��܂��B����� 3 ��̔z���Ԃ��A�e��͎���\���܂��B 
  
- XLL �̊��S�p�X�ƃt�@�C����
    
- XLL からエクスポートされた UDF またはコマンドの名前
    
- 戻り値と引数コード文字列
    
> [!NOTE]
> [!����] XLL �t�@�C������G�N�X�|�[�g���ꂽ�Ƃ��̖��O�́AExcel ���F�����Ă��� UDF �܂��̓R�}���h�̓o�^���Ƃ͈�v���Ȃ��\��������܂��B 
  
Excel 2007 �ȍ~�́A���̓c�[�� (ATP) �֐��͊��S�ɑg�ݍ��܂�Ă���AC API �ɂ́APRICE �� **xlfPrice** �Ȃǂ̊֐��ɑ΂��邻�̓Ǝ��̗񋓑̂�����܂��B�ȑO�̃o�[�W�����ł́A���������֐��̎g�p�ɂ́A **xlUDF** ��g�p����K�v������܂����B�A�h�C���� Excel 2003 ����� Excel 2007 �ȍ~�̃o�[�W�����Ŏg���K�v������A�A�h�C�������������֐���g���ꍇ�A���[�U�[���ŐV�o�[�W��������肵�āA�K�؂ȕ��@�Ŋ֐���Ăяo���K�v������܂��B 
  
## <a name="examples"></a>例

���̗�́A���s���� Excel �̃o�[�W������ 2003 �ȑO�̏ꍇ�ɁAATP �֐� **PRICE** ��Ăяo�� **xlUDF** �֐���\���Ă��܂��B�O���[�o�� �o�[�W�����ϐ� (���̗�ł� **gExcelVersion12plus** �Ȃ�) �̐ݒ�ɂ��ẮA [���ʌ݊���](backward-compatibility.md) ��Q�Ƃ��Ă��������B
  
> [!NOTE]
> [!����] ���̗�ł́A�t���[�����[�N�֐� **TempNum**�A **TempStrConst** ��g�p���A��������� Excel �� C API ��Ăяo���悤�ɐݒ肵�Ă��܂��B 
  
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

�C���v���[�X�ň�����ύX���āA�l��Ԃ� XLL �֐���Ăяo���Ă�A **xlUDF** �֐��͂���܂łǂ���A���� **XLOPER/XLOPER12** �̃A�h���X��g�p���Ēl��Ԃ��܂��B�܂�A�ʏ�� return �X�e�[�g�����g��p���邩�̂悤�ɂ��Č��ʂ�Ԃ��܂��B�߂�l�Ɏg�p���������ɑΉ����� **XLOPER/XLOPER12** �͕ύX����Ă��܂���B���Ƃ��΁A���� 2 �� UDF ��l���Ă݂Ă��������B 
  
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

**UDF \_ 2 が** UDF **\_ 1** を呼び出す場合 **、excel12** の呼び出し後に **pxArg** の **値は変更されず、UDF_1** によって返される値は **xRetVal** に含まれる。
  
���̕��@�� UDS �ւ̌Ăяo���񐔂𑽂��s���ꍇ�A�܂��ŏ��� [xlfEvaluate �֐�](xlfevaluate.md)��g�p���Ċ֐��̖��O��]���ł��܂��B���̌��ʂ̐��́A **xlfRegister** �֐����Ԃ��o�^ ID �Ɠ����ŁA�֐����̑���� **xlUDF** �֐��ւ̍ŏ��̈����Ƃ��ēn�����Ƃ��ł��܂��B����ɂ�� Excel �́A�֐����̌���������K�v�ȏꍇ�ɔ�ׁA��葬���֐�������A�Ăяo�����Ƃ��ł��܂��B 
  
## <a name="see-also"></a>関連項目

- [���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Excel XLL SDK の概要](getting-started-with-the-excel-xll-sdk.md)

