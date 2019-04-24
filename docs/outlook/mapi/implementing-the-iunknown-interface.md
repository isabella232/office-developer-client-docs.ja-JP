---
title: IUnknown インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310046"
---
# <a name="implementing-the-iunknown-interface"></a>IUnknown インターフェイスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドは、すべての MAPI オブジェクトに実装されており、オブジェクト間の通信とオブジェクトの管理をサポートしています。 
  
 **iunknown**には、次の3つのメソッドがあります。 [iunknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)、 [iunknown::: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)、および[iunknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)。 **QueryInterface**では、1つのオブジェクトが特定のインターフェイスをサポートしているかどうかを判断できます。 **QueryInterface**では、互いの機能に関する知識を持たない2つのオブジェクトが対話できます。 **QueryInterface**を実装するオブジェクトが問題のインターフェイスをサポートしている場合は、インターフェイスの実装へのポインターを返します。 要求されたインターフェイスがオブジェクトでサポートされていない場合は、MAPI_E_INTERFACE_NOT_SUPPORTED 値を返します。 
  
**QueryInterface**は、要求されたインターフェイスポインターを返すときに、新しいオブジェクトの参照カウントも増加させる必要があります。 オブジェクトの参照カウントは、オブジェクトの寿命を管理するために使用する数値です。 参照カウントが1より大きい場合は、オブジェクトのメモリが使用されているため、解放できません。 参照カウントが0になるのは、オブジェクトが安全に解放される場合のみです。 
  
他の2つの**IUnknown**メソッドである**AddRef**と**Release**は、参照カウントを管理します。 **AddRef**は参照カウントをインクリメントしますが、**リリース**は減少します。 **QueryInterface**などのインターフェイスポインターを返すメソッドまたは API 関数はすべて、 **AddRef**を呼び出して参照カウントをインクリメントする必要があります。 インターフェイスポインターを受け取るメソッドのすべての実装は、ポインターが不要になったときに、 **Release**を呼び出してカウントを減らす必要があります。 **Release**は既存の参照カウントをチェックし、count が0の場合にのみ、インターフェイスに関連付けられているメモリを解放します。 
  
> [!NOTE]
> **AddRef**と**Release**は正確な値を返す必要がないため、これらのメソッドの呼び出し元は、オブジェクトがまだ有効であるか、破棄されているかを判断するために、戻り値を使用することはできません。 
  
## <a name="see-also"></a>関連項目



[MAPI オブジェクトの実装](implementing-mapi-objects.md)

