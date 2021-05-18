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
  
すべての MAPI オブジェクトに [実装されている IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) インターフェイスのメソッドは、オブジェクト間通信とオブジェクト管理をサポートします。 
  
 **IUnknown には**[、IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) [、IUnknown::QueryInterface、](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)および [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)の 3 つのメソッドがあります。 **QueryInterface を使用** すると、あるオブジェクトが別のオブジェクトが特定のインターフェイスをサポートするかどうかを判断できます。 **QueryInterface を使用** すると、相互の機能に関する事前の知識を持つ 2 つのオブジェクトを操作できます。 **QueryInterface** を実装するオブジェクトが、対象のインターフェイスをサポートしている場合は、インターフェイスの実装へのポインターを返します。 オブジェクトが要求されたインターフェイスをサポートしていない場合は、オブジェクトの値MAPI_E_INTERFACE_NOT_SUPPORTEDします。 
  
**QueryInterface が要求** されたインターフェイス ポインターを返す場合は、新しいオブジェクトの参照カウントも増やす必要があります。 オブジェクトの参照カウントは、オブジェクトのライフスパンを管理するために使用される数値です。 参照カウントが 1 より大きい場合、オブジェクトのメモリはアクティブに使用されているので解放できません。 参照カウントが 0 に低下した場合にのみ、オブジェクトを安全に解放できます。 
  
他の **2 つの IUnknown** メソッドである **AddRef** メソッドと **Release メソッドは**、参照カウントを管理します。 **AddRef は** 参照カウントをインクリメントし **、Release** は参照カウントをデクリメントします。 **QueryInterface** などのインターフェイス ポインターを返すすべてのメソッドまたは API 関数は、参照カウントをインクリメントするために **AddRef** を呼び出す必要があります。 インターフェイス ポインターを受信するメソッドのすべての実装は、ポインターが不要になったときにカウントをデクレメントするために **Release** を呼び出す必要があります。 **リリース** は、既存の参照カウントをチェックし、カウントが 0 の場合にのみインターフェイスに関連付けられているメモリを解放します。 
  
> [!NOTE]
> **AddRef** と **Release** は正確な値を返す必要はないので、これらのメソッドの呼び出し元は戻り値を使用して、オブジェクトがまだ有効か破棄されたのかを判断する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI オブジェクトの実装](implementing-mapi-objects.md)

