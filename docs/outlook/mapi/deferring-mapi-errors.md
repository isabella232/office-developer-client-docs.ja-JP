---
title: MAPI �G���[�ۗ̕�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0cf56a92190acfab1a941bc8d3ad0acc1f3e1f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338704"
---
# <a name="deferring-mapi-errors"></a>MAPI �G���[�ۗ̕�

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
�C���^�[�t�F�C�X�̂������̕��@�ł́A���̓p�����[�^�[�Ƃ��� MAPI_DEFERRED_ERRORS �t���O��������܂��B���̃t���O���ݒ肳��Ă���ꍇ�A���@���Ȃ��l�̒���ɖ߂�ɂ͌�ŁA�Ăяo���̌��ʂ�m�蔭�M�҂ɂ��Ƃ��ł��܂��B
  
Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations. 
  
�T�[�r�X �v���o�C�_�[���G���[�Ɋ֌W�Ȃ�����A�ۗ��N���C�A���g��Ăяo���Ƃ� MAPI_DEFERRED_ERRORS �t���O��ݒ肷�邾���ŏ����ł���x�������Ȃ��A�܂��� MAPI_E_TOO_COMPLEX ��擾���܂��B�قƂ�ǂ̃N���C�A���g�́A�ʘb�����s���邱�Ƃ�����ߐ헪�Ƃ��ăG���[��ۗ�����K�v������܂��B 
  
Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>関連項目



[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)

