---
title: 構成プロパティ シートの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421313"
---
# <a name="displaying-configuration-property-sheets"></a>構成プロパティ シートの表示

**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーは、 [imapisupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用して構成プロパティシートを実装します。 **doconfigpropsheet**を呼び出すと、トランスポートプロバイダーは、プロパティの配列へのポインターと、プロパティの表示方法に関する情報を渡します。 その後、MAPI は標準のダイアログボックスを使って、ユーザーにプロパティを提示します。 一貫性のあるインターフェイスをユーザーに提供することにより、トランスポートプロバイダーを実装する場合は、このプロパティシート機構を使用することを強くお勧めします。
  
## <a name="transport-providers"></a>トランスポートプロバイダー

トランスポートプロバイダーは[builddisplaytable](builddisplaytable.md)関数を使用して、 **doconfigpropsheet**で使用する表示テーブルの構造を簡素化できます。 トランスポートプロバイダーは、プロパティシート API を直接使用することもできます。 プロパティに対する変更をバッファリングするために、トランスポートプロバイダーは[createiprop](createiprop.md)関数を使用できます。 これにより、ユーザーがプロパティに格納されている値を変更している間、ユーザーによる取り消しの処理が簡略化されます。 必要に応じて、トランスポートプロバイダーは、ユーザーの構成タスクを簡素化するためのウィザードダイアログボックスを提供することもできます。 
  

