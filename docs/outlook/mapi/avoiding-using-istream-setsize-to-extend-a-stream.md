---
title: istreamsetsize を使用してストリームを拡張するのを避ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331641"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>IStream:: SetSize を使用してストリームを拡張することを回避する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストリームに書き込む場合、初期サイズが十分ではなくなったので、ストリームを拡大する必要があります。 **istream:: SetSize**ではなく、OLE メソッド**istream:: Write**を使用して、これを実行します。 **IStream:: Write**は自動的に stream を拡張するため、* * IStream:: SetSize * * は不要です。 istream の呼び出し: **:** istream なしで Write **:: setsize**は、**作成**前に**setsize**呼び出しを行うより最大3倍高速です。
  

