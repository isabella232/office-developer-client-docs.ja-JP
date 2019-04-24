---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317500"
---
# <a name="ifreebusydata"></a>IFreeBusyData

特定のユーザーについて、時間範囲を取得および設定し、この時間範囲内のデータの空き時間ブロックを列挙するためのインターフェイスを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |空き時間情報プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[enumblocks](ifreebusydata-enumblocks.md) <br/> |指定した時間範囲内のユーザーのデータの空き時間ブロックを列挙するインターフェイスを取得します。  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[setfbrange アウト](ifreebusydata-setfbrange.md) <br/> |ユーザーのデータの空き時間ブロックの列挙時間の範囲を設定します。  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[getfbpublishrange](ifreebusydata-getfbpublishrange.md) <br/> |ユーザーのデータの空き時間ブロックの列挙の事前設定の時間範囲を取得します。  <br/> |
   
## <a name="remarks"></a>解説

このインターフェイスのメンバーのほとんどは、Outlook の内部使用のために予約されたプレースホルダーであり、変更される可能性があります。 空き時間情報プロバイダーは、指定された値のみを実装する必要があり、指定された戻り値のみを返します。
  
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)
- [定数 (空き時間情報 API)](constants-free-busy-api.md)

