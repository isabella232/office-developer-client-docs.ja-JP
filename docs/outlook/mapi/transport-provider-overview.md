---
title: トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f189ed78d7feb1714fa2a04bf29403c6d33773af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609321"
---
# <a name="transport-provider-overview"></a>トランスポート プロバイダーの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーは、MAPI サブシステムと 1 つ以上の基になるメッセージング システム間の仲介として機能するダイナミック リンク ライブラリ (DLL) です。 メッセージング システムとは、メッセージが送信および受信される特定のメカニズムです。 メッセージング システムの例を次に示します。
  
- トランスポート プロバイダーがメッセージを直接書き込む共有ネットワーク ファイル システム。
    
- トランスポート プロバイダーがメッセージング サーバーへの接続に使用する TCP/IP ネットワーク インターフェイス。
    
- ユーザーが接続するオンライン サービス。
    
- ホスト ベースのメッセージングまたは Office オートメーション システム。
    
- メッセージング サーバーへのリモート プロシージャ呼び出しのセット。
    
- あるコンピューターから別のコンピューターにデータを転送するために使用できるもの。
    
トランスポート プロバイダー DLL は、MAPI で指定されたインターフェイスに準拠している必要があります。 トランスポート プロバイダーの開発者は、メッセージング システムに存在する機能の観点からこのインターフェイスを実装します。
  

