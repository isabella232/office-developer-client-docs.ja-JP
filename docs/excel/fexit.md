---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit function [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798870"
---
# <a name="fexit"></a>fExit

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
GENERIC.xll をアンロードするユーザー定義コマンドの例。GENERIC.xll が読み込まれると、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。  
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ̓p�����[�^�[�͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��́A��� 1 ��Ԃ��܂��B
  
## <a name="remarks"></a>����

����� GENERIC.xll �I�����邽�߂Ƀ��[�U�[���J�n���郋�[�`UNREGISTER("GENERIC.XLL")`UNREGISTER("GENERIC.XLL")` ��Ăяo�����Ƃ͔����K�v������܂��B����͋����I�ɁA���� DLL ��̂��ׂĂ̊֐���o�^������܂��B�����̊֐������̂����ꂩ�ɓo�^����Ă���ꍇ������ł��B���̑���ɁA������ 1 �̊֐���o�^������܂��B 
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

