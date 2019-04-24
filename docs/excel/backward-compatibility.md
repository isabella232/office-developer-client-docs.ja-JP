---
title: 下位互換機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- バージョン互換性 [excel 2007],XLL 互換性 [Excel 2007],下位互換性 [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301681"
---
# <a name="backward-compatibility"></a>下位互換機能

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
このトピックでは、Microsoft Excel の各バージョンにおける XLL 互換性の問題について説明します。
  
## <a name="useful-constant-definitions"></a>便利な定数の定義

XLL プロジェクト コードに、次に示すような定義を組み込んで、このコンテキストで使用されるすべてのリテラルによる数値のインスタンスを置き換えることを検討してください。これにより、バージョン固有のコードが明確になり、バージョンに関連する一見無害な形の数値によるバグが発生する可能性を抑えられるようになります。
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>実行中のバージョンの取得

You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer. For Microsoft Excel 2013, this is 15.0. You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function. You can then set a global variable that informs all of the modules in your project which version of Excel is running. Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.
  
C API �̃o�[�W��������o���邽�߂� **XLCallVer** ��Ăяo�����Ƃ��ł��܂����A���̕��@�ł́AExcel 2007 ���O�̂ǂ̃o�[�W��������s���Ă��邩�ɂ��Ă͎�����܂���B 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>デュアル インターフェイスをエクスポートするアドインの作成

1 つの文字列を受け取り、ワークシートのデータ型のいずれかになる 1 つの値を返す XLL 関数について考えてみましょう。"PD" 型として登録され、次に示すようにプロトタイプされた関数をエクスポートできます。文字列は、長さカウント付きバイト文字列として渡されています。
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
����͊����ɓ��삵�܂����A�������̗��R����AExcel 2007 �ȍ~�̃R�[�h�ɑ΂��闝�z�I�ȃC���^�[�t�F�C�X�ɂ͂Ȃ�܂���B
  
- C API �̃o�C�g������Ɋւ��鐧�����������AExcel 2007 �ȍ~�ŃT�|�[�g����钷�� Unicode ������ɃA�N�Z�X�ł��܂���B
    
- Excel 2007 �ȍ~�� Excel �́A **XLOPER** �̎󂯓n�����\�ł��B�������A����͓���I�� **XLOPER12** �ɕϊ�����邽�߁AExcel 2007 �ȍ~�ł́A�ȑO�� Excel �̃o�[�W�����̃R�[�h�Ŏ��s����ꍇ�ɂ͑��݂��Ȃ��ÖٓI�ȕϊ��̃I�[�o�[�w�b�h���������܂��B
    
- ���̊֐��̓X���b�h �Z�[�t�ɂ���Ă���\��������܂����A�^������  `PD$` �ɕύX�����ƁAExcel 2007 �ȍ~�ł͓o�^�Ɏ��s���܂��B
    
�����̗��R����AExcel 2007 �ȍ~�ł�  `QD%$` �Ƃ��ēo�^����Ă������[�U�[�ɑ΂��āA�R�[�h���X���b�h �Z�[�t�ł���Ƒz�肵�āA���̂悤�Ƀv���g�^�C�v���ꂽ�֐���G�N�X�|�[�g����K�v������܂��B
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Excel 2007 �ȍ~�ł͕ʂ̊֐���o�^���邱�Ƃ��]�܂������ 1 �̗��R�́AXLL �֐����ő� 255 �̈�����󂯓���� (�ȑO�̃o�[�W�����ł� 30 �ɐ�������Ă��܂���)�B
  
�D�s���Ȃ��ƂɁA�v���W�F�N�g���痼���̃o�[�W������G�N�X�|�[�g����ƁA�����̃����b�g�������܂��B���̌�A���s���� Excel �o�[�W��������o���āA�œK�Ȋ֐������ɂ���ēo�^���܂��B�ڍׂƎ�����ɂ��ẮA�u[Excel 2007 �̃A�h�C�� (XLLs) �̊J��](https://msdn.microsoft.com/library/aa730920.aspx)�v��Q�Ƃ��Ă��������B
  
このアプローチでは、同じワークシートを Excel 2003 で実行した場合と、Excel 2007 以降で実行した場合では、異なる結果が表示される可能性があります。たとえば、Excel 2003 では Excel 2003 ワークシート セル内の Unicode 文字列を ASCII バイト文字列にマッピングし、その文字列を切り詰めてから XLL 関数に渡します。Excel 2007 以降の Excel では、適切な方法で登録された XLL 関数に、変換されていない Unicode 文字列を渡します。これが、異なる結果の原因になります。このような可能性とユーザーへの影響に対する注意は、アップグレード時以外にも必要になります。たとえば、いくつかの組み込みの数値関数は、Excel 2000 と Excel 2003 との間で改善されています。
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>新しいワークシート関数と分析ツール関数

Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007. Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md). Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h. The example in Calling User-defined Functions from DLLs demonstrates the two different methods.
  
## <a name="see-also"></a>関連項目

- [C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Excel での C API を使用したプログラミング](programming-with-the-c-api-in-excel.md)
- [Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)

