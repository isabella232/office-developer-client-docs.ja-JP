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
  
トランスポート プロバイダーは [、IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) メソッドを使用して構成プロパティ シートを実装します。 **DoConfigPropSheet を呼** び出す場合、トランスポート プロバイダーはプロパティの配列へのポインターと、プロパティの表示方法に関する情報を渡します。 MAPI は、標準のダイアログ ボックスを使用してユーザーにプロパティを表示します。 一貫性のあるインターフェイスをユーザーに提供する利点のために、トランスポート プロバイダーを実装する場合は、このプロパティ シートメカニズムを使用してください。
  
## <a name="transport-providers"></a>トランスポート プロバイダー

トランスポート プロバイダーは [、BuildDisplayTable](builddisplaytable.md) 関数を使用して **、DoConfigPropSheet** で使用する表示テーブルの構築を簡略化できます。 トランスポート プロバイダーは、プロパティ シート API を直接使用することもできます。 プロパティの変更をバッファー処理するために、トランスポート プロバイダーは [CreateIProp 関数を使用](createiprop.md) できます。 これにより、ユーザーがプロパティに格納されている値を変更する間、ユーザーによる取り消しの処理が簡略化されます。 必要に応じて、トランスポート プロバイダーは、ユーザーの構成タスクを簡略化するためのウィザード ダイアログ ボックスを提供することもできます。 
  

