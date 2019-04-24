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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328274"
---
# <a name="mapi-programming-overview"></a>MAPI プログラミングの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この Microsoft Outlook Messaging API (MAPI) リファレンスは、C および C++ 開発者がさまざまなニーズに対応し、メッセージングを利用するために作成されています。 MAPI を使用してメッセージング機能を備えたアプリケーションを拡張する開発者にとって、特定の前提条件となる知識は必要ありません。 メッセージングおよびコンポーネントオブジェクトモデル (COM) を使用して MAPI を使用し、専用のメッセージングシステムサービスに対してフルスケールのワークグループアプリケーションまたはドライバーを作成する必要があります。
  
開発作業を開始する前に、MAPI の使用方法、ログオンプロセス、プロファイルとメッセージサービスの作成および構成方法に関する以下の情報を考慮する必要があります。
  
メッセージングアプリケーションプログラムインターフェイス (MAPI) は、開発者がメールが有効なアプリケーションを作成するために使用できる豊富な機能セットです。 完全な関数ライブラリは MAPI と呼ばれます。 MAPI を使用すると、クライアントコンピューター上のメッセージングシステムを完全に制御し、メッセージの作成と管理、クライアントメールボックスの管理、サービスプロバイダーなどを行うことができます。
  
> [!NOTE]
> 拡張 mapi は mapi と同じであり、mapi ドキュメントでは単に mapi と呼ばれます。 
  
 **簡易 MAPI**
  
簡易 MAPI には、Microsoft Windows ベースのアプリケーションに対して、基本的なレベルのメッセージング機能を追加できるようにする一連の関数が用意されています。
  
> [!IMPORTANT]
> 簡易 MAPI 関数 MAPISendMail は、microsoft outlook 2013 および microsoft outlook 2010 でサポートされています。 Windows では、他の簡単な MAPI 機能は廃止されました。 
  

