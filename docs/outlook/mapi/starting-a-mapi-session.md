---
title: MAPI セッションを開始
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d683d5fc959b219569417c74494cb47d7c2c059e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804000"
---
# <a name="starting-a-mapi-session"></a>MAPI セッションを開始

  
  
**適用されます**: Outlook 
  
セッション開始時に実行される作業のかなりの量ですが、必要な作業は最小限にします。 この作業の大半は、MAPI で作業が[生じます](mapiinitialize.md)し、 [MAPILogonEx](mapilogonex.md)の呼び出しの処理です。 どちらの関数は、セッション通知の処理とユーザー インターフェイスなどの側面を制御するための入力パラメーターとしてフラグを受け入れます。 MAPI ライブラリを初期化するために**生じます**し、MAPI サブシステムにログオンする**MAPILogonEx**を呼び出すときに、これらのフラグを設定することの影響をよく理解するのには重要です。 
  
 **MAPI セッションを開始するには**
  
1. MAPI ライブラリの標準セットを初期化するために**生じます**を呼び出します。 
    
2. OLE ライブラリを使用する場合は、 [OleInitialize](http://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)の OLE 関数を呼び出します。
    
3. MAPI ユーティリティ ライブラリを使用する場合は、 [ScInitMapiUtil](scinitmapiutil.md)を呼び出します。
    
4. **MAPILogonEx**は、MAPI サブシステムにログオンするための有効なプロファイルを使用して呼び出します。 **MAPILogonEx**では、各プロファイルに含まれているメッセージ サービスのサービス プロバイダーを必要と考えられる場合の詳細についてユーザーに確認の構成を確認します。 **MAPILogonEx**が完了すると、構成済みのサービス プロバイダーは、サービスの準備が完了です。 
    
## <a name="in-this-section"></a>このセクションの内容

[MAPI を初期化しています。](initializing-mapi.md)
  
> セッションの MAPI を初期化する方法について説明します。
    
[MAPI の OLE の初期化](initializing-ole-for-mapi.md)
  
> MAPI を使用するための OLE を初期化するための呼び出しについて説明します。
    
[MAPI ユーティリティを初期化しています。](initializing-the-mapi-utilities.md)
  
> MAPI ユーティリティを初期化する方法について説明します。
    
[MAPI にログオンします。](logging-on-to-mapi.md)
  
> クライアント アプリケーションが MAPI サブシステムにログオンする方法について説明します。
    

