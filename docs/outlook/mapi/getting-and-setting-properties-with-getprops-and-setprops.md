---
title: GetProps および SetProps によるプロパティの取得と設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8bc60dd8241062abb45523393aaf2025ddac03b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614116"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>GetProps および SetProps によるプロパティの取得と設定
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
可能な限り [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドと [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを使用してプロパティを取得または変更してください。 操作するプロパティが非常に大きい場合を指定しない限り、これらのメソッドは適切です。 もう 1 つの方法は [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスを使用してストリームから読み取りまたはストリームに書き込む方法です。 ストリームは非常に大きなプロパティを正常に処理できますが、COM ライブラリが必要なので、リソースの消耗が大きくなります。 **IStream インターフェイスは****、IMAPIProp::GetProps** または **IMAPIProp::SetProps** の呼び出しが失敗した後にのみ使用します。 
  

