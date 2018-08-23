---
title: MAPI �Z�b�V�����̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8c82ff28dca4fc50c7801a533f7ad757b839cddf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568232"
---
# <a name="mapi-session-handling"></a>MAPI �Z�b�V�����̏���

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーと、基になるメッセージング システムと通信するには、セッションを確立する必要があります。 MAPI セッションは、クライアントからその他の MAPI コンポーネントへのリンクです。 結果として正常にセッションを開始、MAPI クライアントに返しますセッション オブジェクトへのポインター、 **IMAPISession**インターフェイスを実装するオブジェクトです。 詳細についてを参照してください[IMAPISession: IUnknown](imapisessioniunknown.md)。 アドレス帳、メッセージ ストア プロバイダーのオブジェクトにアクセスする、いくつかのテーブルにアクセス、フォームを表示する、トランスポート プロバイダーのプロパティを設定およびプロファイルおよびメッセージ サービス管理を実行するのには、 **IMAPISession**インターフェイスのメソッドを使用できます。 
  
## <a name="in-this-section"></a>このセクションの内容

[MAPI セッションの開始](starting-a-mapi-session.md)
  
> MAPI セッションを開始する方法について説明しより詳細な情報を含むトピックへのリンクが含まれています。
    
[MAPI セッションの終了](ending-a-mapi-session.md)
  
> MAPI セッションを終了する方法について説明します。
    
[セッションを使用したオブジェクトへのアクセス](accessing-objects-by-using-the-session.md)
  
> セッション オブジェクトにアクセスするセッションのポインターを使用する方法について説明します。
    
[プライマリとプロバイダー ID の取得](retrieving-primary-and-provider-identity.md)
  
> プロバイダーの id、プライマリを取得するためのプロパティについて説明します。
    
[状態テーブルと状態オブジェクト](status-table-and-status-objects.md)
  
> 状態テーブルから情報にアクセスする方法をについて説明します。
    

