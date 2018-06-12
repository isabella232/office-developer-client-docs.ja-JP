---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798956"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���[�U�[�� Excel �Z�b�V�������ɃA�h�C�� �}�l�[�W���[��g�p���� XLL ��L���ɂ��邽�тɁAMicrosoft Excel �ɂ���Ēǉ�����܂��BExcel ���N�����A���炩���߃C���X�g�[�����ꂽ�A�h�C����ǂݍ��ލۂɂ́A���̊֐��͌Ăяo����܂���B
  
���Ƃ��΁A���̊֐���g�p���āA�A�h�C�����L���ɂȂ��Ă��邱�Ƃ���[�U�[�ɒʒm����J�X�^�� �_�C�A���O �{�b�N�X�̕\���A���W�X�g���̓ǂݎ��Ə������݁A���C�Z���X���̊m�F�Ȃǂ��ł��܂��B
  
Excel �ł́A�����̊֐��̎����ƃG�N�X�|�[�g�� XLL �͕K�v����܂���B
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数の実装では、1 を返す必要があります。 (**int**) です。
  
## <a name="remarks"></a>����

�A�h�C�� �}�l�[�W���[���C�ӂ̃^�X�N��ǉ�����Ƃ��ɁA���̃^�X�N�� XLL �����s����K�v������ꍇ�́A���̊֐���g�p���܂��B
  
## <a name="example"></a>��

���̊֐��̎�����ɂ��ẮA `\SAMPLES\EXAMPLE\EXAMPLE.C` ��  `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B���̃R�[�h�́A  `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[xlAutoRemove](xlautoremove.md)


[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

