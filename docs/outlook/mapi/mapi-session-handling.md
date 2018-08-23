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
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801456"
---
# <a name="mapi-session-handling"></a>MAPI �Z�b�V�����̏���

  
  
**適用対象**: Outlook 
  
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
    

