---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798765"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Excel Calculation ���������ꂽ���Ƃ�N���X�^�[ �R�l�N�^�ɒʒm���܂��B���̂��߁A���̃Z�b�V�����ɂ����ĕۗ����̊֐��̂��ׂĂ̌Ăяo������������\��������܂� (���� Excel �ł́A���ʂ𔺂��R�[���o�b�N�͕K�v����܂���)�B
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>�p�����[�^�[

_セッション Id_
  
> �������ꂽ�v�Z�Ŏg�p����Ă���Z�b�V������ ID �ł��B���̒l�́A[OpenSession](opensession.md) �ɂ���ĕԂ��ꂽ�l�ƈ�v���܂��B
    
## <a name="return-value"></a>�߂�l

**SessionId** �������������ꍇ�� _xlHpcRetSuccess_�A **SessionId** �������������Ȃ��ꍇ�� _xlHpcRetInvalidSessionId_�A���̑��̏�Q�̏ꍇ�� **xlHpcRetCallFailed** �ł��B 
  
## <a name="remarks"></a>����

���̌Ăяo����Ɏ󂯎�錋�ʂ͂��ׂ� Excel �ɂ���Ĕj������邽�߁A�p�t�H�[�}���X����コ����ɂ́A�������ŃZ�b�V�����̂��ׂẴv���Z�X���~����K�v������܂��B
  
## <a name="see-also"></a>�֘A����

- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

