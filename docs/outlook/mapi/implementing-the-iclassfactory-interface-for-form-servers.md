---
title: フォーム サーバーの IClassFactory インターフェイスを実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800952"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>フォーム サーバーの IClassFactory インターフェイスを実装します。

  
  
**適用されます**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx)は、フォーム サーバーのメッセージ クラスの新しいフォームのオブジェクトを作成するクライアント アプリケーションを使用している OLE インターフェイスです。 必要な**IClassFactory**メソッドを次の表に示します。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |新しいフォーム オブジェクトを作成します。  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |複数のフォーム オブジェクトが作成されたときに、起動時のオーバーヘッドを回避できますようにメモリ内でフォームのサーバーをロックします。  <br/> |
   
についてはすべて、これらのメソッドを実装するために必要な Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。
  
## <a name="see-also"></a>関連項目



[フォーム サーバー コードの記述](writing-form-server-code.md)

