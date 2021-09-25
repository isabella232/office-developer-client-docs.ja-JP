---
title: MAPI �Z�b�V�����̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 24a3c7bf89d23cddb6dda5344b01aead2ca38a3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575506"
---
# <a name="mapi-session-handling"></a>MAPI �Z�b�V�����̏���

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーおよび基になるメッセージング システムと通信する前に、セッションを確立する必要があります。 MAPI セッションは、クライアントから他の MAPI コンポーネントへのリンクです。 セッションを正常に開始した結果、MAPI は **、IMAPISession** インターフェイスを実装するオブジェクトであるセッション オブジェクトへのポインターをクライアントに返します。 詳細については [、「IMAPISession : IUnknown 」を参照してください](imapisessioniunknown.md)。 **IMAPISession** インターフェイスのメソッドを使用して、アドレス帳およびメッセージ ストア プロバイダーのオブジェクトにアクセスし、複数のテーブルにアクセスし、フォームを表示し、トランスポート プロバイダーのプロパティを設定し、プロファイルとメッセージ サービスの管理を実行できます。 
  
## <a name="in-this-section"></a>このセクションの内容

[MAPI セッションの開始](starting-a-mapi-session.md)
  
> MAPI セッションを開始する方法について説明し、詳細な情報を含むトピックへのリンクを含む。
    
[MAPI セッションの終了](ending-a-mapi-session.md)
  
> MAPI セッションを終了する方法について説明します。
    
[セッションを使用したオブジェクトへのアクセス](accessing-objects-by-using-the-session.md)
  
> セッション ポインターを使用してセッション オブジェクトにアクセスする方法について説明します。
    
[プライマリ ID とプロバイダー ID の取得](retrieving-primary-and-provider-identity.md)
  
> プライマリ ID とプロバイダー ID を取得するために使用されるプロパティについて説明します。
    
[Status Table オブジェクトと Status オブジェクト](status-table-and-status-objects.md)
  
> 状態テーブルから情報にアクセスする方法について説明します。
    

