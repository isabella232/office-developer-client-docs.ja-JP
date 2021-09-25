---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: 78419e6d4e6e8d4fd44cd76cf5ae542e7231007b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572236"
---
# <a name="ifreebusydata"></a>IFreeBusyData

特定のユーザーの場合は、時間範囲を取得して設定し、この時間範囲内のデータの空き時間情報ブロックを列挙するインターフェイスを返します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |空き時間情報プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[プレースホルダー 1](ifreebusydata-placeholder1.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |指定した時間範囲内のユーザーのデータの空き時間情報ブロックを列挙するインターフェイスを取得します。  <br/> |
|[プレースホルダー 2](ifreebusydata-placeholder2.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[プレースホルダー 3](ifreebusydata-placeholder3.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[プレースホルダー 4](ifreebusydata-placeholder4.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[プレースホルダー 5](ifreebusydata-placeholder5.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |ユーザーのデータの空き時間情報ブロックの列挙の時間範囲を設定します。  <br/> |
|[プレースホルダー 6](ifreebusydata-placeholder6.md) <br/> | *このメンバーはプレースホルダーであり、サポートされていません。*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |ユーザーのデータの空き時間情報ブロックの列挙の事前設定された時間範囲を取得します。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスのメンバーの大部分は、内部で使用するために予約されたプレースホルダーであり、Outlook変更される場合があります。 空き時間情報プロバイダーは、指定した戻り値のみを返す、指定しただけ実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)
- [定数 (空き時間情報 API)](constants-free-busy-api.md)

