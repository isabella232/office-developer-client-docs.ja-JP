---
title: メッセージストアプロバイダーの読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307806"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="3b6de-103">メッセージストアプロバイダーの読み込み</span><span class="sxs-lookup"><span data-stu-id="3b6de-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="3b6de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b6de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b6de-105">クライアントアプリケーションがメッセージストアを開くと、MAPI はメッセージストアプロバイダーの DLL をメモリに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3b6de-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="3b6de-106">mapi によって DLL が読み込まれると、メッセージストアプロバイダーと mapi との間でメソッド呼び出しの特定のシーケンスが発生します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="3b6de-107">このメソッド呼び出しシーケンスを使用すると、mapi はトップレベルの[IMSProvider: iunknown](imsprovideriunknown.md)、 [IMSLogon: iunknown](imslogoniunknown.md)、および[IMsgStore: imapiprop](imsgstoreimapiprop.md)インターフェイスを取得し、メッセージストアプロバイダーが mapi サポートオブジェクトを取得することを許可します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="3b6de-108">呼び出しシーケンスの後、メッセージストアプロバイダーはクライアントからのログオンを受け入れる準備ができている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b6de-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="3b6de-109">メッセージプロバイダ DLL が読み込まれるときの呼び出しシーケンスは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="3b6de-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="3b6de-110">クライアントは[imapisession:: openmsgstore](imapisession-openmsgstore.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="3b6de-111">メッセージストアがまだ開かれていない場合、MAPI はストアプロバイダーの dll を読み込んで、dll の[msproviderinit](msproviderinit.md)エントリポイントを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="3b6de-112">メッセージストアが既に開いている場合は、手順2および3がスキップされ、既存の[IMSProvider: IUnknown](imsprovideriunknown.md)インターフェイスを使用して手順4を完了します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="3b6de-113">**msproviderinit**は、 **IMSProvider**オブジェクトを作成して返します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="3b6de-114">MAPI calls [IMSProvider:: Logon](imsprovider-logon.md)は、クライアントアプリケーションのメッセージストアエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="3b6de-115">**IMSProvider:: Logon**は[IMSLogon: iunknown](imslogoniunknown.md)インターフェイスと[IMsgStore: imapiprop](imsgstoreimapiprop.md)インターフェイスを作成して返し、その[imapiprop: iunknown](imapisupportiunknown.md)インターフェイスで[iunknown](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="3b6de-116">クライアントのメッセージストアのエントリ識別子が既に開かれているメッセージストアを参照している場合、メッセージストアプロバイダーは既存の**IMSLogon**および**IMsgStore**インターフェイスを返すことができ、サポートオブジェクトに対して**AddRef**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3b6de-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="3b6de-117">クライアントが MAPI_NO_MAIL フラグを設定していない場合に、手順1で MDB_NO_MAIL を設定しなかった場合は、mapi スプーラーがメッセージストアにログオンできるように、mapi がメッセージストアのエントリ識別子を mapi スプーラーに提供します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="3b6de-118">MAPI は、クライアントへの**IMsgStore**インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="3b6de-119">MAPI スプーラーは[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="3b6de-120">**IMSProvider:: SpoolerLogon**は、手順5と同じ**IMSLogon**および**IMsgStore**インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="3b6de-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3b6de-121">間違ったパスワードが入力され、メッセージストアプロバイダーが正しいパスワードを要求するインターフェイスを表示できないために、メッセージストアプロバイダーへのログオン呼び出しが失敗する場合は、 **IMSProvider:: logon から MAPI_E_FAILONEPROVIDER を返す必要があります。** メソッド。</span><span class="sxs-lookup"><span data-stu-id="3b6de-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="3b6de-122">これにより、クライアントはユーザーにパスワードの入力を要求して、MAPI がプロバイダーにセッション全体で失敗するのではなく、もう一度メッセージストアプロバイダーへのログオンを試みることができます。</span><span class="sxs-lookup"><span data-stu-id="3b6de-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b6de-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b6de-123">See also</span></span>



[<span data-ttu-id="3b6de-124">MAPI メッセージ ストア プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="3b6de-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

