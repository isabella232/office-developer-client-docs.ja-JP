---
title: 下位互換性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- version compatibility [excel 2007],XLL compatibility [Excel 2007],backward compatibility [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798771"
---
# <a name="backward-compatibility"></a>下位互換性

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���̃g�s�b�N�ł́AMicrosoft Excel �̊e�o�[�W�����ɂ����� XLL �݊����̖��ɂ��Đ�����܂��B
  
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

## <a name="getting-the-running-version"></a>実行中のバージョンを取得します。

バージョンを使用して実行しているを検出する必要があります`Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`、 `arg` **XLOPER**が 2 に設定する数値は、バージョンは、 **XLOPER**を整数値に強制的に変換する文字列です。 Microsoft Excel 2013 では、これは 15.0 です。 または、 [xlAutoOpen](xlautoopen.md)関数でこれを行う必要があります。 すべての Excel のバージョンを実行して、プロジェクト内のモジュールに通知するためのグローバル変数を設定できます。 **Excel12**および**XLOPER12**の s を使用して、 **Excel4** **XLOPER**の s を使用してを使用してまたは C の API を呼び出すか、コードを選択できます。
  
C API �̃o�[�W��������o���邽�߂� **XLCallVer** ��Ăяo�����Ƃ��ł��܂����A���̕��@�ł́AExcel 2007 ���O�̂ǂ̃o�[�W��������s���Ă��邩�ɂ��Ă͎�����܂���B 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>デュアル インターフェイスをエクスポートするアドインを作成します。

1 �̕������󂯎��A���[�N�V�[�g�̃f�[�^�^�̂����ꂩ�ɂȂ� 1 �̒l��Ԃ� XLL �֐��ɂ��čl���Ă݂܂��傤�B"PD" �^�Ƃ��ēo�^����A���Ɏ����悤�Ƀv���g�^�C�v���ꂽ�֐���G�N�X�|�[�g�ł��܂��B������́A�����J�E���g�t���o�C�g������Ƃ��ēn����Ă��܂��B
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
����͊����ɓ��삵�܂����A�������̗��R����AExcel 2007 �ȍ~�̃R�[�h�ɑ΂��闝�z�I�ȃC���^�[�t�F�C�X�ɂ͂Ȃ�܂���B
  
- C API �̃o�C�g������Ɋւ��鐧�����������AExcel 2007 �ȍ~�ŃT�|�[�g����钷�� Unicode ������ɃA�N�Z�X�ł��܂���B
    
- Excel 2007 �ȍ~�� Excel �́A **XLOPER** �̎󂯓n�����\�ł��B�������A����͓���I�� **XLOPER12** �ɕϊ�����邽�߁AExcel 2007 �ȍ~�ł́A�ȑO�� Excel �̃o�[�W�����̃R�[�h�Ŏ��s����ꍇ�ɂ͑��݂��Ȃ��ÖٓI�ȕϊ��̃I�[�o�[�w�b�h���������܂��B
    
- ���̊֐��̓X���b�h �Z�[�t�ɂ���Ă���\��������܂����A�^������  `PD$` �ɕύX�����ƁAExcel 2007 �ȍ~�ł͓o�^�Ɏ��s���܂��B
    
�����̗��R����AExcel 2007 �ȍ~�ł�  `QD%$` �Ƃ��ēo�^����Ă������[�U�[�ɑ΂��āA�R�[�h���X���b�h �Z�[�t�ł���Ƒz�肵�āA���̂悤�Ƀv���g�^�C�v���ꂽ�֐���G�N�X�|�[�g����K�v������܂��B
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Excel 2007 �ȍ~�ł͕ʂ̊֐���o�^���邱�Ƃ��]�܂������ 1 �̗��R�́AXLL �֐����ő� 255 �̈�����󂯓���� (�ȑO�̃o�[�W�����ł� 30 �ɐ�������Ă��܂���)�B
  
�D�s���Ȃ��ƂɁA�v���W�F�N�g���痼���̃o�[�W������G�N�X�|�[�g����ƁA�����̃����b�g�������܂��B���̌�A���s���� Excel �o�[�W��������o���āA�œK�Ȋ֐������ɂ���ēo�^���܂��B�ڍׂƎ�����ɂ��ẮA�u[Excel 2007 �̃A�h�C�� (XLLs) �̊J��](http://msdn.microsoft.com/en-us/library/aa730920.aspx)�v��Q�Ƃ��Ă��������B
  
���̃A�v���[�`�ł́A�������[�N�V�[�g�� Excel 2003 �Ŏ��s�����ꍇ�ƁAExcel 2007 �ȍ~�Ŏ��s�����ꍇ�ł́A�قȂ錋�ʂ��\�������\��������܂��B���Ƃ��΁AExcel 2003 �ł� Excel 2003 ���[�N�V�[�g �Z����� Unicode ������� ASCII �o�C�g������Ƀ}�b�s���O���A���̕������؂�l�߂Ă��� XLL �֐��ɓn���܂��BExcel 2007 �ȍ~�� Excel �ł́A�K�؂ȕ��@�œo�^���ꂽ XLL �֐��ɁA�ϊ�����Ă��Ȃ� Unicode �������n���܂��B���ꂪ�A�قȂ錋�ʂ̌����ɂȂ�܂��B���̂悤�ȉ\���ƃ��[�U�[�ւ̉e���ɑ΂��钍�ӂ́A�A�b�v�O���[�h���ȊO�ɂ�K�v�ɂȂ�܂��B���Ƃ��΁A�������̑g�ݍ��݂̐��l�֐��́AExcel 2000 �� Excel 2003 �Ƃ̊Ԃŉ��P����Ă��܂��B
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>新しいワークシート関数と分析ツール関数

分析ツール (ATP) 関数は、Excel 2007 で Excel の一部です。 以前は、XLL は ATP 関数を呼び出す[xlUDF](xludf.md)を使用して、可能性がありますだけです。 Excel 2007 以降では、分析ツール関数が呼び出される xlcall.h で定義されている関数の列挙体を使用します。 Dll から関数を呼び出すユーザー定義の例は、2 つの方法を示します。
  
## <a name="see-also"></a>�֘A����

- [C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md) 
- [Excel �ł� C API ��g�p�����v���O���~���O](programming-with-the-c-api-in-excel.md)
- [Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)

