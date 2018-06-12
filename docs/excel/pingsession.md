---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798951"
---
# <a name="pingsession"></a>PingSession

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�Z�b�V�������L�����ǂ�����`�F�b�N���܂��B���̊֐��͒ʏ�A�ȑO�Ԃ��ꂽ�Z�b�V���� ID �����݂�A�N�e�B�u�Ŏg�p�\���ǂ����� Excel �Ŕ��f����K�v������ꍇ�ɌĂяo����܂��B
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>�p�����[�^�[

_セッション Id_
  
> ping ����s����Z�b�V������ ID �B���̒l�́A�O�� [OpenSession](opensession.md) ��Ăяo�����ۂɕԂ��ꂽ ID �ƈ�v����K�v������܂� �B
    
## <a name="return-value"></a>�߂�l

**SessionId** �������L���̏ꍇ�� _xlHpcRetSuccess_�A����ȊO�̏ꍇ�� **xlHpcRetInvalidSessionId**�B
  
## <a name="see-also"></a>�֘A����

- [OpenSession](opensession.md)
- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

