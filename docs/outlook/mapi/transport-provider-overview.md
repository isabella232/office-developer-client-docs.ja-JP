---
title: トランスポートプロバイダーの概要
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
# <a name="transport-provider-overview"></a>トランスポートプロバイダーの概要

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーは、MAPI サブシステムと1つ以上の基礎となるメッセージングシステムとの間の仲介として機能するダイナミックリンクライブラリ (DLL) です。 メッセージングシステムは、メッセージを送受信するための特定のメカニズムです。 メッセージングシステムの例として、次のようなものがあります。
  
- トランスポートプロバイダーがメッセージを直接書き込む共有ネットワークファイルシステム。
    
- トランスポートプロバイダーがメッセージングサーバーに接続するために使用する tcp/ip ネットワークインターフェイス。
    
- ユーザーが接続するオンラインサービス。
    
- ホストベースのメッセージングまたは office automation システム。
    
- メッセージングサーバーへのリモートプロシージャ呼び出しのセット。
    
- あるコンピューターから別のコンピューターにデータを転送するために使用できるすべてのもの。
    
トランスポートプロバイダー DLL は、MAPI で指定されているインターフェイスに準拠している必要があります。 トランスポートプロバイダーの開発者は、メッセージングシステムに存在する機能の観点から、このインターフェイスを実装します。
  

