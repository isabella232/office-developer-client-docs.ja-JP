---
title: メッセージ ストア プロバイダーの読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 47b209b9a8818cf235b7c28593da5778dd944989
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568701"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="772e9-103">メッセージ ストア プロバイダーの読み込み</span><span class="sxs-lookup"><span data-stu-id="772e9-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="772e9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="772e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="772e9-105">クライアント アプリケーションは、メッセージ ストアを開いたら、MAPI は、メッセージ ストア プロバイダーの DLL をメモリに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="772e9-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="772e9-106">MAPI には、DLL が読み込まれたら、メッセージ ストア プロバイダーが、MAPI の間で非常に特定、一連のメソッド呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="772e9-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="772e9-107">このメソッドの呼び出し順序が最上位レベルを取得するための MAPI を有効に[IMSProvider: IUnknown](imsprovideriunknown.md)、 [IMSLogon: IUnknown](imslogoniunknown.md)、および[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)インターフェイス、およびメッセージ ストア プロバイダーは、MAPI のサポート オブジェクトを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="772e9-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="772e9-108">呼び出しシーケンスの後メッセージ ストア プロバイダーがクライアントからのログオンを使用する準備があります。</span><span class="sxs-lookup"><span data-stu-id="772e9-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="772e9-109">メッセージ プロバイダー DLL が読み込まれたときに、呼び出しシーケンスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="772e9-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="772e9-110">クライアントは、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="772e9-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="772e9-111">メッセージ ・ ストアが既に開いていない場合は、MAPI ストア プロバイダーの DLL を読み込むし、DLL の[MSProviderInit](msproviderinit.md)エントリ ポイントを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="772e9-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="772e9-112">メッセージ ・ ストアが既に開いている場合は、MAPI 2 および 3 の手順をスキップし、使用して既存の[IMSProvider: IUnknown](imsprovideriunknown.md)手順 4 を完了するためのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="772e9-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="772e9-113">**MSProviderInit**は、作成し、 **IMSProvider**オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="772e9-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="772e9-114">MAPI では、 [IMSProvider::Logon](imsprovider-logon.md)、クライアント アプリケーションのメッセージ ストアのエントリの識別子を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="772e9-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="772e9-115">**IMSProvider::Logon**を作成して返します、 [IMSLogon: IUnknown](imslogoniunknown.md)インタ フェースと[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)インターフェイスとに[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="772e9-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="772e9-116">クライアントのメッセージを格納する場合は、エントリの識別子は既に開かれているメッセージ ・ ストアを参照、メッセージ ストア プロバイダーは既存の**IMSLogon**と**IMsgStore**のインターフェイスを返すことができ、そのサポート オブジェクトの**AddRef**を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="772e9-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="772e9-117">クライアントでは、MAPI_NO_MAIL フラグを設定していない場合とログオンしている、手順 1 では、MAPI、MDB_NO_MAIL を設定していないことにより、メッセージ ストアのエントリの識別子 MAPI スプーラーを MAPI スプーラーは、メッセージ ・ ストアにログオンできるようにします。</span><span class="sxs-lookup"><span data-stu-id="772e9-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="772e9-118">MAPI では、 **IMsgStore**インターフェイスをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="772e9-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="772e9-119">MAPI スプーラーは、 [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="772e9-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="772e9-120">**IMSProvider::SpoolerLogon**は、手順 5 から**IMSLogon**と**IMsgStore**の同じインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="772e9-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="772e9-121">ログオン呼び出しメッセージは、正しくないパスワードが指定されましたが、メッセージ ストア プロバイダーは、正しいパスワードを要求するインターフェイスを表示できないためにプロバイダーが失敗した場合を保存する場合は、 **IMSProvider::Logon から MAPI_E_FAILONEPROVIDER が返す必要があります。** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="772e9-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="772e9-122">これは、パスワードをもう一度ではなく全体のセッションでプロバイダーが失敗するための MAPI メッセージ ストア プロバイダーへのログオンを実行するユーザーを要求するクライアントが許可されます。</span><span class="sxs-lookup"><span data-stu-id="772e9-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="772e9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="772e9-123">See also</span></span>



<span data-ttu-id="772e9-124">[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="772e9-124">[Developing a MAPI Message Store Provider](developing-a-mapi-message-store-provider.md)</span></span>

