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
ms.openlocfilehash: 96e2ca38391931508dd9f3f78f3ba69e6f8b9c15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801276"
---
# <a name="loading-message-store-providers"></a>メッセージ ストア プロバイダーの読み込み

  
  
**適用対象**: Outlook 
  
クライアント アプリケーションは、メッセージ ストアを開いたら、MAPI は、メッセージ ストア プロバイダーの DLL をメモリに読み込みます。 MAPI には、DLL が読み込まれたら、メッセージ ストア プロバイダーが、MAPI の間で非常に特定、一連のメソッド呼び出しが発生します。 このメソッドの呼び出し順序が最上位レベルを取得するための MAPI を有効に[IMSProvider: IUnknown](imsprovideriunknown.md)、 [IMSLogon: IUnknown](imslogoniunknown.md)、および[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)インターフェイス、およびメッセージ ストア プロバイダーは、MAPI のサポート オブジェクトを取得することができます。 呼び出しシーケンスの後メッセージ ストア プロバイダーがクライアントからのログオンを使用する準備があります。 
  
メッセージ プロバイダー DLL が読み込まれたときに、呼び出しシーケンスは次のとおりです。
  
1. クライアントは、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を呼び出します。
    
2. メッセージ ・ ストアが既に開いていない場合は、MAPI ストア プロバイダーの DLL を読み込むし、DLL の[MSProviderInit](msproviderinit.md)エントリ ポイントを呼び出します。 メッセージ ・ ストアが既に開いている場合は、MAPI 2 および 3 の手順をスキップし、使用して既存の[IMSProvider: IUnknown](imsprovideriunknown.md)手順 4 を完了するためのインターフェイスです。 
    
3. **MSProviderInit**は、作成し、 **IMSProvider**オブジェクトを返します。 
    
4. MAPI では、 [IMSProvider::Logon](imsprovider-logon.md)、クライアント アプリケーションのメッセージ ストアのエントリの識別子を渡すことを呼び出します。
    
5. **IMSProvider::Logon**を作成して返します、 [IMSLogon: IUnknown](imslogoniunknown.md)インタ フェースと[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)インターフェイスとに[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、 [IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。 クライアントのメッセージを格納する場合は、エントリの識別子は既に開かれているメッセージ ・ ストアを参照、メッセージ ストア プロバイダーは既存の**IMSLogon**と**IMsgStore**のインターフェイスを返すことができ、そのサポート オブジェクトの**AddRef**を呼び出す必要はありません。 
    
6. クライアントでは、MAPI_NO_MAIL フラグを設定していない場合とログオンしている、手順 1 では、MAPI、MDB_NO_MAIL を設定していないことにより、メッセージ ストアのエントリの識別子 MAPI スプーラーを MAPI スプーラーは、メッセージ ・ ストアにログオンできるようにします。
    
7. MAPI では、 **IMsgStore**インターフェイスをクライアントに返します。 
    
8. MAPI スプーラーは、 [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)を呼び出します。
    
9. **IMSProvider::SpoolerLogon**は、手順 5 から**IMSLogon**と**IMsgStore**の同じインターフェイスを返します。 
    
> [!NOTE]
> ログオン呼び出しメッセージは、正しくないパスワードが指定されましたが、メッセージ ストア プロバイダーは、正しいパスワードを要求するインターフェイスを表示できないためにプロバイダーが失敗した場合を保存する場合は、 **IMSProvider::Logon から MAPI_E_FAILONEPROVIDER が返す必要があります。** メソッドです。 これは、パスワードをもう一度ではなく全体のセッションでプロバイダーが失敗するための MAPI メッセージ ストア プロバイダーへのログオンを実行するユーザーを要求するクライアントが許可されます。 
  
## <a name="see-also"></a>関連項目



[MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)

