---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317627"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートします。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |空き時間情報プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |列挙の空き時間情報データの次に指定したブロック数を取得します。  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |空き時間情報データの指定された数のブロックをスキップします。  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |カーソルを先頭に設定して、列挙子をリセットします。  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |列挙を指定した期間に制限します。  <br/> |
   
## <a name="remarks"></a>注釈

列挙には、時間内に重複しないデータの空き時間情報ブロックが含まれています。 予定表に重複するアイテムがある場合、Outlook は、これらのアイテムを結合して、次の優先順位 (アウトオブオフィス、ビジー、暫定的) に基づいて、列挙内の重複しない空き時間情報ブロックを形成します。
  
空き時間情報プロバイダーは [、IFreeBusyData](ifreebusydata.md)を使用して、ユーザーの時間範囲のこのインターフェイスと列挙を取得します。
  
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [定数 (空き時間情報 API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

