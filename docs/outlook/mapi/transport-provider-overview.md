---
title: トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804143"
---
# <a name="transport-provider-overview"></a>トランスポート プロバイダーの概要

  
  
**適用対象**: Outlook 
  
トランスポート プロバイダーは、MAPI のサブシステムと 1 つまたは複数の基になるメッセージング システムとの間の媒介手段として機能するダイナミック リンク ライブラリ (DLL) です。 メッセージング システムは、メッセージの送信し、受信はいくつか特定のメカニズムです。 メッセージング システムのいくつかの例は次のとおりです。
  
- トランスポート プロバイダーは、直接にメッセージを書き込み共有ネットワーク ・ ファイル ・ システムです。
    
- トランスポート プロバイダーを使用して、メッセージング サーバーへの接続に TCP/IP ネットワーク インターフェイスです。
    
- ユーザーに接続するオンライン サービスです。
    
- ホスト ・ ベースのメッセージや、office オートメーション システム。
    
- メッセージング サーバーへのリモート プロシージャ呼び出しのセットです。
    
- 1 台のコンピューター間でデータを転送するに使用できるものです。
    
トランスポート プロバイダー DLL は、MAPI によって指定されたインターフェイスに従う必要があります。 トランスポート プロバイダー開発者は、メッセージング システム内の機能には、このインターフェイスを実装します。
  

