---
title: �ėp DLL �̊֐�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798898"
---
# <a name="functions-in-the-generic-dll"></a>�ėp DLL �̊֐�

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�t�H���_�[  `\EXAMPLES\GENERIC\` �ɂ́A�T���v���� DLL GENERIC.xll ��R���p�C�����邽�߂ɕK�v�� Microsoft Visual Studio �̃v���W�F�N�g �t�@�C���ƃ\�[�X �R�[�h �t�@�C�����܂܂�Ă��܂��B���̃v���W�F�N�g��e���v���[�g�Ƃ��Ďg�p���ēƎ��� Microsoft Excel XLL ��쐬�ł��܂��B���̃v���W�F�N�g�̃\�[�X �R�[�h�ɂ́AExcel C API �̑����̋@�\��������Ă��܂��B 
  
GENERIC.xll ��ǂݍ��ނƁA���� 4 �̃R�}���h������ **[Generic]** ���j���[���쐬����܂��B 
  
- **Dialog** - [Microsoft Excel] �_�C�A���O �{�b�N�X��\�����܂��B 
    
- **ダンス**- は、 **ESC**キーを押すまで選択範囲を移動します。 
    
- **Native Dialog** - [Windows] �_�C�A���O �{�b�N�X��\�����܂��B 
    
- **Exit** - GENERIC.xll ��A�����[�h���A **[Generic]** ���j���[��폜���܂��B 
    
GENERIC.xll �͂܂��A���[�N�V�[�g�֐� Func1�AFuncSum�A����� FuncFib ��񋟂��܂��B�����͂��ł� GENERIC.xll ���ǂݍ��܂�Ă���Ƃ��Ɏg�p�ł��܂��BGENERIC.xll �́A�A�h�C�� �}�l�[�W���[��g�p���ēǂݍ��ނ��Ƃ��ł��܂��B�Ō�� Excel �Z�b�V����������ɏI���������_�ŃA�N�e�B�u�ɂȂ��Ă����ꍇ�́A���̎��̃Z�b�V�����ł�ǂݍ��܂�܂��B
  
���̃v���W�F�N�g�ł́A�t���[�����[�N ���C�u���� (FRMWRK32.lib) ��g�p���܂��B
  
## <a name="in-this-section"></a>このセクションの内容

[DIALOGMsgProc](dialogmsgproc.md)
  
[ExcelCursorProc](excelcursorproc.md)
  
[HookExcelWindow](hookexcelwindow.md)
  
[UnhookExcelWindow](unhookexcelwindow.md)
  
[fShowDialog](fshowdialog.md)
  
[fDance](fdance.md)
  
[fDialog/fDialog12](fdialog-fdialog12.md)
  
[fExit](fexit.md)
  
[Func1](func1.md)
  
[FuncSum](funcsum.md)
  
[FuncFib](funcfib.md)
  
## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

