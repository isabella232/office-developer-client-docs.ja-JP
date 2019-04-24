---
title: MAPI プロパティのエラーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1dc676101d4c39544c9dd1fae94000db9963ea02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299391"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="337e9-103">MAPI プロパティのエラーの処理</span><span class="sxs-lookup"><span data-stu-id="337e9-103">Handling MAPI property errors</span></span>

<span data-ttu-id="337e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="337e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="337e9-105">�S�ʓI�Ɏ��s�����܂��͐��������ꍇ�́A����ɂ́A���� **IMAPIProp**���@�́A�����I�Ȑ�����񍐂��܂��B</span><span class="sxs-lookup"><span data-stu-id="337e9-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="337e9-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="337e9-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="337e9-107">setprops による</span><span class="sxs-lookup"><span data-stu-id="337e9-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="337e9-108">deleteprops</span><span class="sxs-lookup"><span data-stu-id="337e9-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="337e9-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="337e9-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="337e9-110">copyprops</span><span class="sxs-lookup"><span data-stu-id="337e9-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="337e9-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span><span class="sxs-lookup"><span data-stu-id="337e9-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="337e9-p102">**IMAPIProp**���̕��@�ł́A�قȂ镔���I�Ȑ�����񍐂��܂��B�����̕��@�ł́AS_OK ��Ԃ�[SPropProblemArray](spropproblemarray.md)�\����̃G���[����z�u���ĕ����I�Ȑ�����񍐂��܂��B���\�b�h�̐����܂��͎��s�������ǂ����Ɋ֌W�Ȃ��f�[�^���܂܂�� **GetProps**�̃v���p�e�B�l�̔z��Ƃ͈قȂ�A���M�҂ɂ́A�G���[�ɂ��Ċw�K���o�^����Ă���ꍇ�ɂ̂݁A�G���[������ꍇ�ɂ݂̂����̕��@�Ńv���p�e�B�̖��̔z�񂪑��݂��܂��B���M�҂ɂ́A�G���[����o�^����L���� **SPropProblemArray**�|�C���^�[��w�肷��K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="337e9-p102">The other **IMAPIProp** methods report partial success differently. These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure. Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors. Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="337e9-p103">**SetProps**�A **DeleteProps**�A **CopyTo**�A�܂��� **CopyProps**����Ԃ��ꂽ�ꍇ�A�G���[�l�A�����̕����ł͂Ȃ��G���[������Ă��܂��B�v���p�e�B���z��ŁA�g�p�\�ȏꍇ�͖����ł��B�N���C�A���g���������\���ɕێ�����Ă���f�[�^�ɃA�N�Z�X����ɂ��Ă�\�����̂������悤�K�v������܂��B�K�؂ȉ�����[IMAPIProp::GetLastError](imapiprop-getlasterror.md)���܂��B</span><span class="sxs-lookup"><span data-stu-id="337e9-p103">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success. The property problem array, if available, is not valid. Clients should not try to access data held in the structure nor should they try to free the structure itself. The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="337e9-p104">**GetLastError**�́AWindows SDK �ɓ������O�̊֐��Ɏ��Ă��܂��B�߂�l�Ŏg�p�ł���ł͂Ȃ����ڍׂȃG���[�Ɋւ�����̑o����񋟂��܂��B���҂́A�O�̃G���[�������������ƂɊւ������Ԃ��܂��B���́AWin32 **GetLastError**�֐��̌Ăяo�����̃X���b�h�ɂ���Đ������ꂽ�G���[ ���|�[�g **IMAPIProp::GetLastError**����݂̃I�u�W�F�N�g�ɂ���Đ������ꂽ�G���[�̕񍐂ł��B�܂�A�N���C�A���g�ł́A���b�Z�[�W�� MAPI_E_NO_ACCESS �� **DeleteProps**��Ăяo���ꍇ�́A���̃��b�Z�[�W�͓ǂݎ���p�A **GetLastError**���b�Z�[�W����񋟂��ꂽ�f�[�^��Ԃ����Ƃ�����Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="337e9-p104">**GetLastError** is similar to the function of the same name provided in the Windows SDK. Both provide more detailed information about an error than is available with the return value. They both return information about the previous error that has occurred. The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object. That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="337e9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="337e9-128">See also</span></span>

- [<span data-ttu-id="337e9-129">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="337e9-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

