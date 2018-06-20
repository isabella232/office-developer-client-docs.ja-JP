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
ms.openlocfilehash: 177bd84addb001970e52801fd2cddba3a8d81706
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801414"
---
# <a name="mapi-programming-overview"></a>MAPI プログラミングの概要

  
  
**適用されます**: Outlook 
  
この Microsoft Outlook メッセージング API (MAPI) の参照は、C に書かれてと、C++ 開発者は、さまざまなニーズし、メッセージが発生します。 開発者にとって、メッセージング機能を持つアプリケーションを拡張するために MAPI を使用する、特定の前提となる知識は必要ありません。 メッセージの背景と、コンポーネント オブジェクト モデル (COM) 本格的なワークグループ アプリケーション、または特殊なメッセージング システムのサービス用のドライバーを作成するのには MAPI を使用する必要があります。
  
開発作業を開始する前に MAPI を使用する方法に関する次の情報を考慮する必要がありますログオン プロセス、およびプロファイルとメッセージ サービスの作成および構成方法。
  
メッセージング アプリケーション プログラム インターフェイス (MAPI) は、メールが有効なアプリケーションを作成する開発者が使用できる関数の拡張セットです。 フル機能のライブラリは、MAPI と呼ばれます。 MAPI は、クライアント コンピューター、作成およびメッセージの管理、クライアントのメールボックス、サービス ・ プロバイダーなどの管理上のメッセージング システムを完全に制御を有効にします。
  
> [!NOTE]
> 拡張 MAPI は MAPI と同じは単と呼ばれるに MAPI MAPI ドキュメントで。 
  
 **簡易 MAPI**
  
簡易 MAPI は、Microsoft Windows ベースのアプリケーションに機能をメッセージングの基本的なレベルを追加することを可能にする一連の関数を提供します。
  
> [!IMPORTANT]
> MAPISendMail 簡易 MAPI の関数は、Microsoft Outlook 2013 と Microsoft Outlook 2010 でサポートされます。 シンプル MAPI の関数は他の Windows になりました。 
  

