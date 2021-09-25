---
title: IStreamDocfile で OLE 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 923d3945d31cf15ccc0262c2628e2b38489054fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625134"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>IStreamDocfile で OLE 添付ファイルを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE オブジェクト添付ファイルを開く場合は、IStream または [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx)ではなく **IStreamDocfile** インターフェイスを使用します。 [](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) 

**IStreamDocfile は** 、構造化ストレージを使用してオブジェクトに直接アクセスできます。コピー操作を実行する必要がなくなります。オーバーヘッドを削減します。 **IStreamDocfile** は **IStream** の特定の実装で、ストリームのコンテンツは構造化ストレージとして書式設定されます。 **IStreamDocfile は** 、メッセージ ストア プロバイダーによって実装されます。 
  

