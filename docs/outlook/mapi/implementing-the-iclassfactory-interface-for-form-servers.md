---
title: フォームサーバー用の IClassFactory インターフェイスの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310032"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>フォームサーバー用の IClassFactory インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)は、クライアントアプリケーションがフォームサーバーのメッセージクラスの新しいフォームオブジェクトを作成するために使用する OLE インターフェイスです。 次の表に、必要な**IClassFactory**メソッドを示します。 
  
|**方法**|**説明**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |新しい form オブジェクトを作成します。  <br/> |
|[lockserver](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |複数のフォームオブジェクトが作成されたときに起動のオーバーヘッドを回避できるように、フォームサーバーをメモリ内にロックします。  <br/> |
   
これらのメソッドを実装するために必要なすべての情報については、Windows SDK の「COM および ActiveX のオブジェクトサービス」セクションを参照してください。
  
## <a name="see-also"></a>関連項目



[フォームサーバーコードの記述](writing-form-server-code.md)

