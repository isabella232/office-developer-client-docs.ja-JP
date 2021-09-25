---
title: MAPI セッションの開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 765bfef3ab30ec4a534f78cc7175394d96d5163c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566382"
---
# <a name="starting-a-mapi-session"></a>MAPI セッションの開始

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションの起動中に実行される作業量は非常に多く、必要なタスクは最小限です。 この作業の多くは [、MAPIInitialize](mapiinitialize.md) 呼び出しと [MAPILogonEx](mapilogonex.md) 呼び出しの MAPI 処理で行われます。 どちらの関数も、通知処理やユーザー インターフェイスなどのセッションの側面を制御するための入力パラメーターとしてフラグを受け入れる。 **MAPIInitialize** を呼び出して MAPI ライブラリを初期化し、MAPI サブシステムにログオンする **MAPILogonEx** を呼び出す場合、これらの各フラグを設定した結果を理解することが重要です。 
  
 **MAPI セッションを開始するには**
  
1. **MAPIInitialize を呼び** 出して、MAPI ライブラリの標準セットを初期化します。 
    
2. OLE ライブラリを使用する必要がある場合は、OLE 関数 [OleInitialize を呼び出します](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)。
    
3. MAPI ユーティリティ ライブラリを使用する必要がある場合は [、ScInitMapiUtil を呼び出します](scinitmapiutil.md)。
    
4. **MAPI サブシステムにログオンする** 有効なプロファイルを使用して MAPILogonEx を呼び出します。 **MAPILogonEx** は、プロファイルに含まれるメッセージ サービス内の各サービス プロバイダーの構成を確認し、必要に応じて、可能な場合は追加情報をユーザーに求めるプロンプトを表示します。 **MAPILogonEx が** 完了すると、構成済みのサービス プロバイダーはサービスの準備が整います。 
    
## <a name="in-this-section"></a>このセクションの内容

[MAPI の初期化](initializing-mapi.md)
  
> セッションの MAPI を初期化する方法について説明します。
    
[OLE for MAPI の初期化](initializing-ole-for-mapi.md)
  
> MAPI で使用するために OLE を初期化する呼び出しについて説明します。
    
[MAPI ユーティリティの初期化](initializing-the-mapi-utilities.md)
  
> MAPI ユーティリティを初期化する方法について説明します。
    
[MAPI へのログオン](logging-on-to-mapi.md)
  
> クライアント アプリケーションが MAPI サブシステムにログオンする方法について説明します。
    

