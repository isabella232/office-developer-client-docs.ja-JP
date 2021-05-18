---
title: MAPI �Z�b�V�����̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422062"
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
    

