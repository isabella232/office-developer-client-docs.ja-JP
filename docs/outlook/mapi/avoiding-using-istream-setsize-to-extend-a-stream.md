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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799749"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>IStream::SetSize を使用してストリームを拡張することを避ける

  
  
**適用されます**: Outlook 
  
、ストリームに書き込むときの初期サイズが十分でないために、それらを拡大する必要があります。 OLE メソッド**IStream::Write**を使用して、これを実現する**IStream::SetSize**ではなく。 **IStream::Write**は、ストリームを自動的に拡張すること * * IStream::SetSize * * 不要な。 **IStream::SetSize**に**IStream::Write**を呼び出すことは、3 回まで呼び出し**を記述**する前に、 **SetSize**を行うよりも高速。
  

