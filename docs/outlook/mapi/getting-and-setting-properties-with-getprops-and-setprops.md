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
  
可能な限り [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドと [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを使用してプロパティを取得または変更してください。 操作するプロパティが非常に大きい場合を指定しない限り、これらのメソッドは適切です。 もう 1 つの方法は [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスを使用してストリームから読み取りまたはストリームに書き込む方法です。 ストリームは非常に大きなプロパティを正常に処理できますが、COM ライブラリが必要なので、リソースの消耗が大きくなります。 **IStream インターフェイスは****、IMAPIProp::GetProps** または **IMAPIProp::SetProps** の呼び出しが失敗した後にのみ使用します。 
  

