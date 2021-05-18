---
title: フォーム サーバーの IClassFactory インターフェイスの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310032"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>フォーム サーバーの IClassFactory インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IClassFactory は](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) 、クライアント アプリケーションがフォーム サーバーのメッセージ クラスの新しいフォーム オブジェクトを作成するために使用する OLE インターフェイスです。 次の表に、 **必要な IClassFactory** メソッドの一覧を示します。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |新しいフォーム オブジェクトを作成します。  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |複数のフォーム オブジェクトを作成するときに起動オーバーヘッドを回避できるよう、フォーム サーバーをメモリにロックします。  <br/> |
   
これらのメソッドを実装するために必要なすべての情報については、SDK の「COM と ActiveX オブジェクト サービス」セクションWindowsしてください。
  
## <a name="see-also"></a>関連項目



[フォーム サーバー コードの作成](writing-form-server-code.md)

