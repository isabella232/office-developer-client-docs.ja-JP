---
title: トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433158"
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
  

