---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: aa42561277d5fc4de93eeedec8ceb6f36530fb80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799343"
---
# <a name="ifreebusydata"></a>IFreeBusyData

特定のユーザーを取得、時間範囲を設定およびこの時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |プロバイダーの空き/予約済み  <br/> |
|インターフェイスの識別子。  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |指定した時間範囲内のユーザーのデータのブロックの空き時間情報を列挙するインターフェイスを取得します。  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |ユーザーの空き時間情報データ ブロックの列挙体の時間の範囲を設定します。  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |ユーザーのデータのブロックの空き時間情報の列挙型の事前に設定された時間の範囲を取得します。  <br/> |
   
## <a name="remarks"></a>備考

このインターフェイスのメンバーのほとんどは、Outlook の内部使用に予約されているプレース ホルダーであるし、変更されることが。 空き/予約済みプロバイダーする必要があります実装のみとして指定した場合は、のみ、指定した戻り値を返します。
  
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)
- [定数 (空き時間情報の API)](constants-free-busy-api.md)

