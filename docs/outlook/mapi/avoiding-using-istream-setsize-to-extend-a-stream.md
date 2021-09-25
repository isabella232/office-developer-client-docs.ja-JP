---
title: IStreamSetSize を使用してストリームを拡張しないようにする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c4df52e6be76bd7844ed4b16912a4e1d7642edfb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584774"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>IStream::SetSize を使用したストリームの拡張の回避

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストリームに書き込む場合、初期サイズが十分ではなくなったため、ストリームを拡大する必要がある場合があります。 OLE メソッド **IStream::Write** を使用して **、IStream::SetSize ではなく、これを実行します**。 **IStream::Write** によってストリームが自動的に拡張され、** IStream::SetSize ** が不要になります。 **IStream::Write** を **IStream::SetSize** なしで呼び出す場合、書き込み前に **SetSize** 呼び出しを行うよりも最大 3 倍速 **くなります**。
  

