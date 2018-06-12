---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove function [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798974"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���[�U�[�� Excel �Z�b�V�������ɃA�h�C�� �}�l�[�W���[��g�p���� XLL �𖳌��ɂ��邽�тɁAMicrosoft Excel �ɂ���ČĂяo����܂��B�A�h�C�����C���X�g�[������Ă����Ԃ� Excel �Z�b�V����������I���A�܂��ُ͈�I������ƁA���̊֐��͌Ăяo����܂���B
  
���Ƃ��΂��̊֐���g�p���āA�A�h�C���������ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X��\��������A���W�X�g���̓ǂݎ��Ə������݂�s�����肷�邱�Ƃ��ł��܂��B
  
Excel �ł́A�����̊֐��̎����ƃG�N�X�|�[�g�� XLL �͕K�v����܂���B 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数の実装では、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>����

�A�h�C�� �}�l�[�W���[�ɂ���ă^�X�N���폜���ꂽ�Ƃ��� XLL �����̃^�X�N���������K�v������ꍇ�́A���̊֐���g�p���܂��B
  
## <a name="example"></a>��

���̊֐��̎���������  `\SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `\SAMPLES\GENERIC\GENERIC.C` �t�@�C����Q�Ƃ��Ă��������B���̃R�[�h�́A  `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[xlAutoAdd](xlautoadd.md)


[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

