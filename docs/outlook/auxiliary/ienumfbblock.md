---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799347"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

アクセスと時間の範囲内でのユーザーのデータのブロックの空き時間情報の列挙をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |プロバイダーの空き/予約済み  <br/> |
|インターフェイスの識別子。  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Next/次のレコード](ienumfbblock-next.md) <br/> |列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。  <br/> |
|[スキップ](ienumfbblock-skip.md) <br/> |指定された空き時間情報データのブロック数をスキップします。  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |先頭にカーソルを設定することにより、列挙子をリセットします。  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。  <br/> |
|[制限します。](ienumfbblock-restrict.md) <br/> |指定した期間内に列挙型を制限します。  <br/> |
   
## <a name="remarks"></a>備考

列挙体には、時間が重複しないデータのブロック空き時間情報にはが含まれています。 これらの項目の優先順位に基づいて列挙体の空き/予約済みブロックの重複を形成する結合 Outlook の予定表に重複する項目がある場合は、: 不在時の予定あり、仮の予定です。
  
空き/予約済みのプロバイダーは、このインターフェイスは、 [IFreeBusyData](ifreebusydata.md)を使用してユーザーの時間範囲の列挙体を取得します。
  
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [定数 (空き時間情報の API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

