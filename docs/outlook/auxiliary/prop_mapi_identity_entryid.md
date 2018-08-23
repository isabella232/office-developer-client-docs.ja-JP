---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: 取得または、アカウントのアドレス帳のエントリ ID を設定します。
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799568"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="f6be1-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f6be1-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="f6be1-104">取得または、アカウントのアドレス帳のエントリ ID を設定します。</span><span class="sxs-lookup"><span data-stu-id="f6be1-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f6be1-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f6be1-105">Quick info</span></span>

<span data-ttu-id="f6be1-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6be1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6be1-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="f6be1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f6be1-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="f6be1-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="f6be1-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="f6be1-109">Property type:</span></span>  <br/> |<span data-ttu-id="f6be1-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6be1-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6be1-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="f6be1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f6be1-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="f6be1-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="f6be1-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="f6be1-113">Access:</span></span>  <br/> |<span data-ttu-id="f6be1-114">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f6be1-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6be1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f6be1-115">Remarks</span></span>

 <span data-ttu-id="f6be1-116">**プロペラ\_MAPI\_の ID\_エントリ ID**のすべてのアカウントの存在ではありません。</span><span class="sxs-lookup"><span data-stu-id="f6be1-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="f6be1-117">たとえば、Exchange アカウントがある**プロペラ\_MAPI\_の ID\_ENTRYID**設定ではなく[プロペラ\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)、SMTP と POP3 アカウントの場合は、逆です。</span><span class="sxs-lookup"><span data-stu-id="f6be1-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="f6be1-118">**プロペラ\_MAPI_IDENTITY_ENTRYID** [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)の_lppEntryID_によって返される値を次のようなエントリ ID を返します。</span><span class="sxs-lookup"><span data-stu-id="f6be1-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6be1-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6be1-119">See also</span></span>

- [<span data-ttu-id="f6be1-120">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="f6be1-120">About the Account Management API</span></span>](about-the-account-management-api.md)

