---
title: フォーム サーバー用 IClassFactory インターフェイスの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388050"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>フォーム サーバー用 IClassFactory インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)は、フォーム サーバーのメッセージ クラスの新しいフォームのオブジェクトを作成するクライアント アプリケーションを使用している OLE インターフェイスです。 必要な**IClassFactory**メソッドを次の表に示します。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |新しいフォーム オブジェクトを作成します。  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |複数のフォーム オブジェクトが作成されたときに、起動時のオーバーヘッドを回避できますようにメモリ内でフォームのサーバーをロックします。  <br/> |
   
についてはすべて、これらのメソッドを実装するために必要な Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。
  
## <a name="see-also"></a>関連項目



[フォーム サーバー コードの記述](writing-form-server-code.md)

