---
title: イベントの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0576687d6bb80f6fc3d5779db3625beccbfbc28c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572397"
---
# <a name="handling-events"></a>イベントの処理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel 2010 以降の XLL は、非同期関数のライフ サイクルを管理するために設計されたイベントを受信できます。これらのイベントは次のとおりです。
  
- **CalculationEnded**: Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。
    
- **CalculationCanceled**: ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、**CalculationEnded** イベントが発生します。 
    
これらのイベントを処理するために、XLL では C API 関数の [xlEventRegister](xleventregister.md) を使用します。 
  
> [!NOTE]
> プログラムによる再計算中は、**CalculationEnded** と **CalculationCanceled** は発生しません。 
  

