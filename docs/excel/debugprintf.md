---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf function [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798769"
---
# <a name="debugprintf"></a>debugPrintf

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Windows SDK �֐� **OutputDebugStringA** ��g�p���āA�A�N�e�B�u�ȃf�o�b�K�[�Ƀk���I�[������̏������݂�s���t���[�����[�N ���C�u�����֐��B�A�v���P�[�V�����Ƀf�o�b�K�[���Ȃ��ꍇ�́A�V�X�e���̃f�o�b�K�[�ɕ����񂪕\������܂��B�A�v���P�[�V�����Ƀf�o�b�K�[���Ȃ��A�V�X�e���̃f�o�b�K�[���A�N�e�B�u�łȂ��ꍇ�́A **debugPrintf** �͉��̓����s���܂���B 
  
���̊֐��͒l��Ԃ��܂���B
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpFormat (LPSTR)_
  
�`��������ŁA **sprintf** �֐��ƂƂ�ɗp�����镶����̍\���ƃ��[���ɏ]���B 
  
 _arguments_
  
�`��������Ɉ�v���� 0 �ȏ�̈����B
  
## <a name="example"></a>��

この関数は、関数にコントロールが渡されたことを示す文字列を印刷します。コンパイルする前に _DEBUG フラグを定義する必要があります。未定義のままでは、この関数は何の動作も行いません。
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

