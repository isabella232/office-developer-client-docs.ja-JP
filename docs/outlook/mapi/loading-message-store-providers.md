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
# <a name="loading-message-store-providers"></a>メッセージストアプロバイダーの読み込み

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションがメッセージストアを開くと、MAPI はメッセージストアプロバイダーの DLL をメモリに読み込みます。 mapi によって DLL が読み込まれると、メッセージストアプロバイダーと mapi との間でメソッド呼び出しの特定のシーケンスが発生します。 このメソッド呼び出しシーケンスを使用すると、mapi はトップレベルの[IMSProvider: iunknown](imsprovideriunknown.md)、 [IMSLogon: iunknown](imslogoniunknown.md)、および[IMsgStore: imapiprop](imsgstoreimapiprop.md)インターフェイスを取得し、メッセージストアプロバイダーが mapi サポートオブジェクトを取得することを許可します。 呼び出しシーケンスの後、メッセージストアプロバイダーはクライアントからのログオンを受け入れる準備ができている必要があります。 
  
メッセージプロバイダ DLL が読み込まれるときの呼び出しシーケンスは次のようになります。
  
1. クライアントは[imapisession:: openmsgstore](imapisession-openmsgstore.md)を呼び出します。
    
2. メッセージストアがまだ開かれていない場合、MAPI はストアプロバイダーの dll を読み込んで、dll の[msproviderinit](msproviderinit.md)エントリポイントを呼び出します。 メッセージストアが既に開いている場合は、手順2および3がスキップされ、既存の[IMSProvider: IUnknown](imsprovideriunknown.md)インターフェイスを使用して手順4を完了します。 
    
3. **msproviderinit**は、 **IMSProvider**オブジェクトを作成して返します。 
    
4. MAPI calls [IMSProvider:: Logon](imsprovider-logon.md)は、クライアントアプリケーションのメッセージストアエントリ識別子を渡します。
    
5. **IMSProvider:: Logon**は[IMSLogon: iunknown](imslogoniunknown.md)インターフェイスと[IMsgStore: imapiprop](imsgstoreimapiprop.md)インターフェイスを作成して返し、その[imapiprop: iunknown](imapisupportiunknown.md)インターフェイスで[iunknown](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。 クライアントのメッセージストアのエントリ識別子が既に開かれているメッセージストアを参照している場合、メッセージストアプロバイダーは既存の**IMSLogon**および**IMsgStore**インターフェイスを返すことができ、サポートオブジェクトに対して**AddRef**を呼び出す必要はありません。 
    
6. クライアントが MAPI_NO_MAIL フラグを設定していない場合に、手順1で MDB_NO_MAIL を設定しなかった場合は、mapi スプーラーがメッセージストアにログオンできるように、mapi がメッセージストアのエントリ識別子を mapi スプーラーに提供します。
    
7. MAPI は、クライアントへの**IMsgStore**インターフェイスを返します。 
    
8. MAPI スプーラーは[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)を呼び出します。
    
9. **IMSProvider:: SpoolerLogon**は、手順5と同じ**IMSLogon**および**IMsgStore**インターフェイスを返します。 
    
> [!NOTE]
> 間違ったパスワードが入力され、メッセージストアプロバイダーが正しいパスワードを要求するインターフェイスを表示できないために、メッセージストアプロバイダーへのログオン呼び出しが失敗する場合は、 **IMSProvider:: logon から MAPI_E_FAILONEPROVIDER を返す必要があります。** メソッド。 これにより、クライアントはユーザーにパスワードの入力を要求して、MAPI がプロバイダーにセッション全体で失敗するのではなく、もう一度メッセージストアプロバイダーへのログオンを試みることができます。 
  
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

