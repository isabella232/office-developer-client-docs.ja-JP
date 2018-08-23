---
title: IStreamSetSize を使用してストリームを拡張することを避ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592081"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>IStream::SetSize を使用したストリーム拡張の回避

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
、ストリームに書き込むときの初期サイズが十分でないために、それらを拡大する必要があります。 OLE メソッド**IStream::Write**を使用して、これを実現する**IStream::SetSize**ではなく。 **IStream::Write**は、ストリームを自動的に拡張すること * * IStream::SetSize * * 不要な。 **IStream::SetSize**に**IStream::Write**を呼び出すことは、3 回まで呼び出し**を記述**する前に、 **SetSize**を行うよりも高速。
  

