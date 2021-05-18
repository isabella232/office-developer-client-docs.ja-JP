---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: アカウントのアドレス帳エントリ ID を取得または設定します。
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326433"
---
# <a name="prop_mapi_identity_entryid"></a><span data-ttu-id="872e6-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="872e6-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="872e6-104">アカウントのアドレス帳エントリ ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="872e6-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="872e6-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="872e6-105">Quick info</span></span>

<span data-ttu-id="872e6-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="872e6-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="872e6-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="872e6-107">Identifier:</span></span>  <br/> |<span data-ttu-id="872e6-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="872e6-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="872e6-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="872e6-109">Property type:</span></span>  <br/> |<span data-ttu-id="872e6-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="872e6-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="872e6-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="872e6-111">Property tag:</span></span>  <br/> |<span data-ttu-id="872e6-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="872e6-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="872e6-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="872e6-113">Access:</span></span>  <br/> |<span data-ttu-id="872e6-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="872e6-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="872e6-115">注釈</span><span class="sxs-lookup"><span data-stu-id="872e6-115">Remarks</span></span>

 <span data-ttu-id="872e6-116">**PROP \_MAPI \_ IDENTITY \_ ENTRYID は** 、すべてのアカウントに存在するとは見なされません。</span><span class="sxs-lookup"><span data-stu-id="872e6-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="872e6-117">たとえば、SMTP/POP3 Exchangeアカウントの場合、PROP **\_ MAPI IDENTITY \_ \_ ENTRYID** を設定し、PROP ACCT_USER_EMAIL_ADDR を設定することはできませんが、SMTP/POP3 アカウントの場合は、状況が元に戻されます。 [ \_](prop_acct_user_email_addr.md)</span><span class="sxs-lookup"><span data-stu-id="872e6-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="872e6-118">**PROP \_MAPI_IDENTITY_ENTRYID** は [、IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx)で _lppEntryID_ によって返される値に似たエントリ ID を返します。</span><span class="sxs-lookup"><span data-stu-id="872e6-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="872e6-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="872e6-119">See also</span></span>

- [<span data-ttu-id="872e6-120">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="872e6-120">About the Account Management API</span></span>](about-the-account-management-api.md)

