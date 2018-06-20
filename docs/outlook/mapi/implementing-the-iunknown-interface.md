---
title: IUnknown インターフェイスを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 55bf8831af8f78767b2607c21ab54c32f6e4245f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800961"
---
# <a name="implementing-the-iunknown-interface"></a>IUnknown インターフェイスを実装します。

  
  
**適用されます**: Outlook 
  
すべての MAPI オブジェクトに実装されている、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドをサポートして通信とオブジェクト管理を決める基準について説明します。 
  
 **IUnknown**には 3 つの方法: [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)、 [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)、および[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)。 **QueryInterface**には、別のオブジェクトが特定のインターフェイスをサポートしているかどうかを決定する 1 つのオブジェクトが有効にします。 **QueryInterface**を持つ他の機能の予備知識がない 2 つのオブジェクトを操作できます。 **QueryInterface**を実装するオブジェクトには、対象のインターフェイスをサポートして場合、は、インターフェイスの実装にポインターを返します。 オブジェクトが要求されたインターフェイスをサポートしていない場合は、MAPI_E_INTERFACE_NOT_SUPPORTED 値を返します。 
  
**QueryInterface**に要求されたインターフェイス ポインターが返されるとき、新しいオブジェクトの参照カウントも増加する必要です。 オブジェクトの参照カウントは、オブジェクトの有効期間を管理するために使用する数値値です。 参照カウントが 1 より大きい場合は、積極的に使用されているため、オブジェクトのメモリを解放できません。 だけすると、リファレンス カウントが 0 にオブジェクトを安全に解放できることをお勧めします。 
  
他の 2 つ**IUnknown**のメソッド、 **AddRef**と**リリース**では、参照カウントを管理します。 **AddRef**は、**リリース**をデクリメントしているときに、参照カウントをインクリメントしています。 すべてのメソッドや、 **QueryInterface**などのインターフェイス ポインターを返すための API 関数は、参照カウントをインクリメントするのに**AddRef**を呼び出す必要があります。 インターフェイス ポインターを受け取るメソッドのすべての実装では、ポインターが不要になったときにカウントをデクリメントする**リリース**を呼び出す必要があります。 **リリース**は、カウントが 0 である場合にのみに、インターフェイスに関連付けられているメモリを解放して、既存の参照カウントを確認します。 
  
> [!NOTE]
> **AddRef**および**Release**は、正確な値を返す必要はありません、ためこれらのメソッドの呼び出し元で必要がありますオブジェクトがまだ有効であるかが破棄されたかどうかを判断するのに戻り値は使用しません。 
  
## <a name="see-also"></a>関連項目



[MAPI オブジェクトを実装します。](implementing-mapi-objects.md)

