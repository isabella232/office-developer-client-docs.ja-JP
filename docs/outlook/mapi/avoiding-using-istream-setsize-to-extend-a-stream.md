---
title: IStreamSetSize を使用してストリームを拡張しないようにする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428915"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>IStream::SetSize を使用したストリームの拡張の回避

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストリームに書き込む場合、初期サイズが十分ではなくなったため、ストリームを拡大する必要がある場合があります。 OLE メソッド **IStream::Write** を使用して **、IStream::SetSize ではなく、これを実行します**。 **IStream::Write** によってストリームが自動的に拡張され、** IStream::SetSize ** が不要になります。 **IStream::Write** を **IStream::SetSize** なしで呼び出す場合、書き込み前に **SetSize** 呼び出しを行うよりも最大 3 倍速 **くなります**。
  

