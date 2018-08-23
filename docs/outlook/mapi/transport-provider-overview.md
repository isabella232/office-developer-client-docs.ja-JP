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
ms.openlocfilehash: dbc56b7334d3966696641a84f23a64ce3802e3e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595273"
---
# <a name="transport-provider-overview"></a>トランスポート プロバイダーの概要

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーは、MAPI のサブシステムと 1 つまたは複数の基になるメッセージング システムとの間の媒介手段として機能するダイナミック リンク ライブラリ (DLL) です。 メッセージング システムは、メッセージの送信し、受信はいくつか特定のメカニズムです。 メッセージング システムのいくつかの例は次のとおりです。
  
- トランスポート プロバイダーは、直接にメッセージを書き込み共有ネットワーク ・ ファイル ・ システムです。
    
- トランスポート プロバイダーを使用して、メッセージング サーバーへの接続に TCP/IP ネットワーク インターフェイスです。
    
- ユーザーに接続するオンライン サービスです。
    
- ホスト ・ ベースのメッセージや、office オートメーション システム。
    
- メッセージング サーバーへのリモート プロシージャ呼び出しのセットです。
    
- 1 台のコンピューター間でデータを転送するに使用できるものです。
    
トランスポート プロバイダー DLL は、MAPI によって指定されたインターフェイスに従う必要があります。 トランスポート プロバイダー開発者は、メッセージング システム内の機能には、このインターフェイスを実装します。
  

