---
title: GetProps および SetProps によるプロパティの取得と設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299399"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>GetProps および SetProps によるプロパティの取得と設定
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
可能な限り、 [imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、プロパティを取得または変更してみてください。 作業しているプロパティが非常に大きい場合以外は、これらのメソッドが適切である必要があります。 もう1つの方法として、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用してストリームの読み取りまたは書き込みを行うことができます。 ストリームは非常に大きなプロパティを正常に処理できますが、COM ライブラリを必要とするため、リソースがより高速に処理されます。 **IStream**インターフェイスは、 **imapiprop:: GetProps**または**imapiprop:: setprops**の呼び出しが失敗した後にのみ使用してください。 
  

