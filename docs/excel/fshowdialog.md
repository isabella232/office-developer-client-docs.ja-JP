---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog function [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798889"
---
# <a name="fshowdialog"></a>fShowDialog

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
ネイティブ Windows ダイアログ ボックスの例を読み込んで表示するユーザー定義コマンドの例です。GENERIC.xll が読み込まれるとき、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ̓p�����[�^�[�͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��́A����Ɋ����������Ƃ���������l 0 ��Ԃ��܂��B
  
## <a name="remarks"></a>����

�l�C�e�B�u Windows �_�C�A���O �{�b�N�X��\������菇�͎��̂Ƃ���ł��B
  
1. **GetHwnd** ��g�p���āAMicrosoft Excel ���C�� �E�B���h�E �n���h����擾���܂��B
    
2. **HookExcelWindow** ��g�p���� Excel ���C�� �E�B���h�E��t�b�N���܂��B
    
3. **DialogBox** �ɂ���ă_�C�A���O �{�b�N�X��\�����܂��B
    
4. **UnhookExcelWindow** ��g�p���� Excel ���C�� �E�B���h�E�̃t�b�N�������܂��B
    
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

