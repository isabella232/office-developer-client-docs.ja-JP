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
ms.openlocfilehash: e2b091fa21dae4a1a8da23954d5f998010483da1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799884"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="c163e-103">MAPI �G���[�ۗ̕�</span><span class="sxs-lookup"><span data-stu-id="c163e-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="c163e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c163e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c163e-p101">�C���^�[�t�F�C�X�̂������̕��@�ł́A���̓p�����[�^�[�Ƃ��� MAPI_DEFERRED_ERRORS �t���O��������܂��B���̃t���O���ݒ肳��Ă���ꍇ�A���@���Ȃ��l�̒���ɖ߂�ɂ͌�ŁA�Ăяo���̌��ʂ�m�蔭�M�҂ɂ��Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="c163e-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="c163e-107">サービス プロバイダーには、高速に処理することを複雑なメソッドの実装では、エラーを保留します。</span><span class="sxs-lookup"><span data-stu-id="c163e-107">Deferring errors helps service providers in their implementation of complex methods, making processing faster.</span></span> <span data-ttu-id="c163e-108">多くの要求を処理し、それぞれの値を返すのではなくエラーを遅延させることは、サービス ・ プロバイダーにバンドルされているへの呼び出しを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c163e-108">Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider.</span></span> <span data-ttu-id="c163e-109">一度に多数の要求を処理パフォーマンスを向上させるため、ネットワーク トラフィックの削減します。</span><span class="sxs-lookup"><span data-stu-id="c163e-109">Processing many requests at once cuts down on network traffic, thereby improving performance.</span></span> <span data-ttu-id="c163e-110">エラーを保留することは、呼び出しを削除またはコピーのプロパティは、非常に時間のかかる操作をすることができます便利です。</span><span class="sxs-lookup"><span data-stu-id="c163e-110">Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="c163e-p103">�T�[�r�X �v���o�C�_�[���G���[�Ɋ֌W�Ȃ�����A�ۗ��N���C�A���g��Ăяo���Ƃ� MAPI_DEFERRED_ERRORS �t���O��ݒ肷�邾���ŏ����ł���x�������Ȃ��A�܂��� MAPI_E_TOO_COMPLEX ��擾���܂��B�قƂ�ǂ̃N���C�A���g�́A�ʘb�����s���邱�Ƃ�����ߐ헪�Ƃ��ăG���[��ۗ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c163e-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="c163e-113">MAPI_DEFERRED_ERRORS を設定するフラグは、返される情報は、予定時刻ではなく、いつでも配信できるという点では、実装を処理するクライアントのエラーを変更します。</span><span class="sxs-lookup"><span data-stu-id="c163e-113">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time.</span></span> <span data-ttu-id="c163e-114">何もそれについて、または元の要求に関するデータが利用できなくすることが遅すぎる場合に返されるエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="c163e-114">It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available.</span></span> <span data-ttu-id="c163e-115">などのクライアントは、MAPI_DEFERRED_ERRORS のセットを使用して削除されたフォルダーを開くには、 **IMsgStore::OpenEntry**を呼び出す、クライアントはわからない問題のフォルダーのプロパティのいずれかを取得するために、 **IMAPIProp::GetProps**の呼び出しが行われるまでです。</span><span class="sxs-lookup"><span data-stu-id="c163e-115">For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties.</span></span> <span data-ttu-id="c163e-116">**GetProps** MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="c163e-116">**GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c163e-117">�֘A����</span><span class="sxs-lookup"><span data-stu-id="c163e-117">See also</span></span>



[<span data-ttu-id="c163e-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c163e-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="c163e-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c163e-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

