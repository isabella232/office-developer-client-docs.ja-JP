---
title: MAPI の機能とアーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2e78f5a9450b16e323bfea3ebb8c01119d2cf3d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567215"
---
# <a name="mapi-features-and-architecture"></a>MAPI の機能とアーキテクチャ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング API (MAPI) は、一般的なアプリケーション プログラミング インターフェイスのセットと、ダイナミック リンク ライブラリ (DLL) コンポーネントで構成されます。 インターフェイスは、多様なメッセージング アプリケーションとメッセージング システムの作成とアクセスに使用され、開発と使用のための均一な環境を提供し、両方に真の独立性を提供します。 DLL には MAPI サブシステムが含まれています。このサブシステムは、フロントエンド メッセージング アプリケーションとバック エンド メッセージング システム間のやり取りを管理し、頻繁なタスクに共通のユーザー インターフェイスを提供します。 MAPI サブシステムは、さまざまなメッセージング システムを統合し、クライアントの違いを保護する中央クリアリングハウスとして機能します。
  
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

