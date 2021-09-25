---
title: メッセージ ストア プロバイダーの読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2cd4cfe3ba259a46752083f12b962c749ef4ce3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595918"
---
# <a name="loading-message-store-providers"></a>メッセージ ストア プロバイダーの読み込み

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションがメッセージ ストアを開くと、MAPI はメッセージ ストア プロバイダーの DLL をメモリに読み込む。 MAPI が DLL を読み込むと、メッセージ ストア プロバイダーと MAPI の間でメソッド呼び出しの非常に特定のシーケンスが発生します。 このメソッドの呼び出しシーケンスを使用すると、MAPI は、トップ レベルの [IMSProvider ( IUnknown](imsprovideriunknown.md)、 [IMSLogon : IUnknown](imslogoniunknown.md)、 および [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) インターフェイス) を取得し、メッセージ ストア プロバイダーが MAPI サポート オブジェクトを取得できます。 呼び出しシーケンスの後、メッセージ ストア プロバイダーはクライアントからのログオンを受け入れる準備ができている必要があります。 
  
メッセージ プロバイダー DLL が読み込まれた場合の呼び出しシーケンスは次のとおりです。
  
1. クライアントは [IMAPISession::OpenMsgStore を呼び出します](imapisession-openmsgstore.md)。
    
2. メッセージ ストアが開いていない場合、MAPI はストア プロバイダーの DLL を読み込み、DLL の [MSProviderInit](msproviderinit.md) エントリ ポイントを呼び出します。 メッセージ ストアが既に開いている場合、MAPI は手順 2 と 3 をスキップし、既存の [IMSProvider : IUnknown](imsprovideriunknown.md) インターフェイスを使用して手順 4 を完了します。 
    
3. **MSProviderInit は****、IMSProvider オブジェクトを作成して返** します。 
    
4. MAPI は、クライアント アプリケーションのメッセージ ストア エントリ識別子を渡す [IMSProvider::Logon](imsprovider-logon.md)を呼び出します。
    
5. **IMSProvider::Logon** は [、IMSLogon : IUnknown](imslogoniunknown.md)インターフェイスと [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)インターフェイスを作成して返し [、IMAPISupport : IUnknown](imapisupportiunknown.md)インターフェイスで [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。 クライアントのメッセージ ストア エントリ識別子が既に開いているメッセージ ストアを参照している場合、メッセージ ストア プロバイダーは既存の **IMSLogon** インターフェイスと **IMsgStore** インターフェイスを返す可能性があります。サポート オブジェクトで **AddRef** を呼び出す必要が生じない。 
    
6. クライアントがログオン時に MAPI_NO_MAIL フラグを設定しなかった場合に、手順 1 で MDB_NO_MAIL を設定しなかった場合、MAPI は MAPI スプーラーにメッセージ ストアのエントリ識別子を与え、MAPI スプーラーはメッセージ ストアにログオンできます。
    
7. MAPI は、 **クライアントに IMsgStore** インターフェイスを返します。 
    
8. MAPI スプーラーは [、IMSProvider::SpoolerLogon を呼び出します](imsprovider-spoolerlogon.md)。
    
9. **IMSProvider::SpoolerLogon** は、手順 5 から同じ **IMSLogon** インターフェイスと **IMsgStore** インターフェイスを返します。 
    
> [!NOTE]
> 正しくないパスワードが指定されたため、メッセージ ストア プロバイダーへのログオン呼び出しが失敗し、メッセージ ストア プロバイダーが正しいパスワードを要求するインターフェイスを表示できない場合は **、IMSProvider::Logon** メソッドから MAPI_E_FAILONEPROVIDER を返す必要があります。 これにより、クライアントは、MAPI がセッション全体のプロバイダーに失敗する代わりに、メッセージ ストア プロバイダーへのログオンを再度試みるパスワードをユーザーに求めるプロンプトを表示できます。 
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

