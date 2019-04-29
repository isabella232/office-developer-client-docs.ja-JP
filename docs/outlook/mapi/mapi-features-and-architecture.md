---
title: MAPI の機能とアーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8156cb53fc81f4861e4a66da4960df0458ec6c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418282"
---
# <a name="mapi-features-and-architecture"></a>MAPI の機能とアーキテクチャ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング API (MAPI) は、一般的なアプリケーションプログラミングインターフェイスのセットと、ダイナミックリンクライブラリ (DLL) コンポーネントで構成されています。 このインターフェイスは、さまざまなメッセージングアプリケーションおよびメッセージングシステムを作成してアクセスし、開発および使用するための一様な環境を提供し、両方に対して真の独立性を提供するために使用されます。 DLL には MAPI サブシステムが含まれており、フロントエンドメッセージングアプリケーションとバックエンドメッセージングシステムの間の相互作用を管理し、頻繁にタスクを行うための共通のユーザーインターフェイスを提供します。 MAPI サブシステムは、さまざまなメッセージングシステムを統合し、それらの違いからクライアントをシールドするための中央クリアリングとして機能します。
  
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

