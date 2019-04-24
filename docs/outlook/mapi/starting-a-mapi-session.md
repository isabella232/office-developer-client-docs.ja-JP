---
title: MAPI セッションの開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336345"
---
# <a name="starting-a-mapi-session"></a>MAPI セッションの開始

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションの起動時に大量の作業が実行されますが、必要なタスクは最小限で済みます。 この作業の多くは、 [MAPIInitialize](mapiinitialize.md)および[MAPILogonEx](mapilogonex.md)呼び出しの MAPI 処理で行われます。 どちらの関数も、通知処理やユーザーインターフェイスなどのセッションの側面を制御するための入力パラメーターとしてフラグを受け入れます。 **MAPIInitialize**を呼び出して mapi ライブラリと**MAPILogonEx**を初期化し、mapi サブシステムにログオンするときに、これらの各フラグを設定した場合の影響を理解しておくことが重要です。 
  
 **MAPI セッションを開始するには**
  
1. **MAPIInitialize**を呼び出して、MAPI ライブラリの標準セットを初期化します。 
    
2. ole ライブラリを使用する必要がある場合は、ole 関数[oleinitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)を呼び出します。
    
3. MAPI ユーティリティライブラリを使用する必要がある場合は、 [ScInitMapiUtil](scinitmapiutil.md)を呼び出してください。
    
4. 有効なプロファイルを使用して**MAPILogonEx**を呼び出して、MAPI サブシステムにログオンします。 **MAPILogonEx**は、プロファイルに含まれているメッセージサービスの各サービスプロバイダーの構成を確認し、必要に応じて、ユーザーに追加情報を要求します。 **MAPILogonEx**が完了すると、構成されたサービスプロバイダーがサービスの準備が整います。 
    
## <a name="in-this-section"></a>このセクションの内容

[MAPI の初期化](initializing-mapi.md)
  
> セッションの MAPI を初期化する方法について説明します。
    
[OLE for MAPI の初期化](initializing-ole-for-mapi.md)
  
> MAPI で使用するために OLE を初期化するために必要な呼び出しについて説明します。
    
[MAPI ユーティリティの初期化](initializing-the-mapi-utilities.md)
  
> MAPI ユーティリティを初期化する方法について説明します。
    
[MAPI へのログオン](logging-on-to-mapi.md)
  
> クライアントアプリケーションが MAPI サブシステムにログオンする方法について説明します。
    

