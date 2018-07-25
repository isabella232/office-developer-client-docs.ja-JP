---
title: イベントの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798877"
---
# <a name="handling-events"></a>イベントの処理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel 2010 以降の XLL は、非同期関数のライフ サイクルを管理するために設計されたイベントを受信できます。これらのイベントは次のとおりです。
  
- **CalculationEnded**: Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。
    
- **CalculationCanceled**: ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、**CalculationEnded** イベントが発生します。 
    
これらのイベントを処理するために、XLL では C API 関数の [xlEventRegister](xleventregister.md) を使用します。 
  
> [!NOTE]
> プログラムによる再計算中は、**CalculationEnded** と **CalculationCanceled** は発生しません。 
  

