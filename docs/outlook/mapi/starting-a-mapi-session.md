---
title: MAPI セッションの開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382590"
---
# <a name="starting-a-mapi-session"></a>MAPI セッションの開始

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション開始時に実行される作業のかなりの量ですが、必要な作業は最小限にします。 この作業の大半は、MAPI で作業が[生じます](mapiinitialize.md)し、 [MAPILogonEx](mapilogonex.md)の呼び出しの処理です。 どちらの関数は、セッション通知の処理とユーザー インターフェイスなどの側面を制御するための入力パラメーターとしてフラグを受け入れます。 MAPI ライブラリを初期化するために**生じます**し、MAPI サブシステムにログオンする**MAPILogonEx**を呼び出すときに、これらのフラグを設定することの影響をよく理解するのには重要です。 
  
 **MAPI セッションを開始するには**
  
1. MAPI ライブラリの標準セットを初期化するために**生じます**を呼び出します。 
    
2. OLE ライブラリを使用する場合は、 [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)の OLE 関数を呼び出します。
    
3. MAPI ユーティリティ ライブラリを使用する場合は、 [ScInitMapiUtil](scinitmapiutil.md)を呼び出します。
    
4. **MAPILogonEx**は、MAPI サブシステムにログオンするための有効なプロファイルを使用して呼び出します。 **MAPILogonEx**では、各プロファイルに含まれているメッセージ サービスのサービス プロバイダーを必要と考えられる場合の詳細についてユーザーに確認の構成を確認します。 **MAPILogonEx**が完了すると、構成済みのサービス プロバイダーは、サービスの準備が完了です。 
    
## <a name="in-this-section"></a>このセクションの内容

[MAPI の初期化](initializing-mapi.md)
  
> セッションの MAPI を初期化する方法について説明します。
    
[OLE for MAPI の初期化](initializing-ole-for-mapi.md)
  
> MAPI を使用するための OLE を初期化するための呼び出しについて説明します。
    
[MAPI ユーティリティの初期化](initializing-the-mapi-utilities.md)
  
> MAPI ユーティリティを初期化する方法について説明します。
    
[MAPI へのログオン](logging-on-to-mapi.md)
  
> クライアント アプリケーションが MAPI サブシステムにログオンする方法について説明します。
    

