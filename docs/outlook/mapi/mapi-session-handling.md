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
  
サービスプロバイダおよび基盤となるメッセージングシステムと通信するには、事前にセッションを確立しておく必要があります。 mapi セッションは、クライアントから他の mapi コンポーネントへのリンクです。 セッションが正常に開始された結果、MAPI はクライアントに session オブジェクトへのポインターを返します。これは、 **imapisession**インターフェイスを実装するオブジェクトです。 詳細については、「 [imapisession: IUnknown](imapisessioniunknown.md)」を参照してください。 **imapisession**インターフェイスのメソッドを使用すると、アドレス帳およびメッセージストアプロバイダーのオブジェクトにアクセスし、複数のテーブルにアクセスしたり、フォームを表示したり、トランスポートプロバイダーのプロパティを設定したり、プロファイルとメッセージサービスの管理を実行したりすることができます。 
  
## <a name="in-this-section"></a>このセクションの内容

[MAPI セッションの開始](starting-a-mapi-session.md)
  
> MAPI セッションを開始する方法について説明し、詳細情報を含むトピックへのリンクを示します。
    
[MAPI セッションの終了](ending-a-mapi-session.md)
  
> MAPI セッションを終了する方法について説明します。
    
[セッションを使用してオブジェクトにアクセスする](accessing-objects-by-using-the-session.md)
  
> セッションポインターを使用して session オブジェクトにアクセスする方法について説明します。
    
[プライマリとプロバイダー id の取得](retrieving-primary-and-provider-identity.md)
  
> プライマリとプロバイダーの id を取得するために使用されるプロパティについて説明します。
    
[状態テーブルと状態オブジェクト](status-table-and-status-objects.md)
  
> 状態テーブルから情報にアクセスする方法について説明します。
    

