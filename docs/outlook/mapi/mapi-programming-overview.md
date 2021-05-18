---
title: MAPI プログラミングの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408342"
---
# <a name="mapi-programming-overview"></a>MAPI プログラミングの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この Microsoft Outlook メッセージング API (MAPI) リファレンスは、メッセージングに関するさまざまなニーズと経験を持つ C および C++ 開発者向けです。 MAPI を使用してメッセージング機能を持つアプリケーションを拡張する開発者向けには、特定の前提条件に関する知識は必要ありません。 MAPI を使用して、専用のメッセージング システム サービス用の本格的なワークグループ アプリケーションまたはドライバーを作成するには、メッセージングのバックグラウンドとコンポーネント オブジェクト モデル (COM) が必要です。
  
開発作業を開始する前に、MAPI の使用方法、ログオン プロセス、およびプロファイルとメッセージ サービスの作成および構成方法に関する次の情報を検討する必要があります。
  
メッセージング アプリケーション プログラム インターフェイス (MAPI) は、開発者がメールが有効なアプリケーションの作成に使用できる広範な機能のセットです。 完全な関数ライブラリは MAPI と呼ばれる。 MAPI を使用すると、クライアント コンピューター上のメッセージング システムの完全な制御、メッセージの作成と管理、クライアント メールボックスの管理、サービス プロバイダーなどです。
  
> [!NOTE]
> 拡張 MAPI は MAPI と同じであり、MAPI ドキュメントでは MAPI と呼ばれます。 
  
 **簡易 MAPI**
  
単純な MAPI には、基本的なレベルのメッセージング機能を Microsoft Windowsベースのアプリケーションに追加できる一連の機能があります。
  
> [!IMPORTANT]
> 単純な MAPI 関数 MAPISendMail は、MAPISendMail のMicrosoft Outlook 2013とMicrosoft Outlook 2010。 その他の単純な MAPI 関数は、この機能でWindows。 
  

