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
# <a name="deferring-mapi-errors"></a><span data-ttu-id="6d038-103">MAPI �G���[�ۗ̕�</span><span class="sxs-lookup"><span data-stu-id="6d038-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="6d038-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d038-p101">�C���^�[�t�F�C�X�̂������̕��@�ł́A���̓p�����[�^�[�Ƃ��� MAPI_DEFERRED_ERRORS �t���O��������܂��B���̃t���O���ݒ肳��Ă���ꍇ�A���@���Ȃ��l�̒���ɖ߂�ɂ͌�ŁA�Ăяo���̌��ʂ�m�蔭�M�҂ɂ��Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="6d038-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="6d038-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span><span class="sxs-lookup"><span data-stu-id="6d038-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="6d038-p103">�T�[�r�X �v���o�C�_�[���G���[�Ɋ֌W�Ȃ�����A�ۗ��N���C�A���g��Ăяo���Ƃ� MAPI_DEFERRED_ERRORS �t���O��ݒ肷�邾���ŏ����ł���x�������Ȃ��A�܂��� MAPI_E_TOO_COMPLEX ��擾���܂��B�قƂ�ǂ̃N���C�A���g�́A�ʘb�����s���邱�Ƃ�����ߐ헪�Ƃ��ăG���[��ۗ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6d038-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="6d038-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="6d038-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6d038-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d038-117">See also</span></span>



[<span data-ttu-id="6d038-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6d038-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="6d038-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6d038-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

