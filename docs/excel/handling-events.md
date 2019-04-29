---
title: �C�x���g�̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438268"
---
# <a name="handling-events"></a>イベントの処理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel 2010 以降の XLL は、非同期関数のライフ サイクルを管理するために設計されたイベントを受信できます。これらのイベントは次のとおりです。
  
- **CalculationEnded**: Excel が計算を完了したときに発生します。計算中に割り当てたリソースは、このイベントの後で解放できます。
    
- **CalculationCanceled**: ユーザーが計算を中断すると発生します。XLL はすべての非同期アクティビティを停止します。このイベントの直後に、**CalculationEnded** イベントが発生します。 
    
これらのイベントを処理するために、XLL では C API 関数の [xlEventRegister](xleventregister.md) を使用します。 
  
> [!NOTE]
> プログラムによる再計算中は、**CalculationEnded** と **CalculationCanceled** は発生しません。 
  

