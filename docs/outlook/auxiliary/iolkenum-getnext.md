---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: 列挙子の次のアカウントを取得します。
ms.openlocfilehash: 7d49faa7bb6be4b0ee76eb36f47a6971dc5b1ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557142"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

列挙子の次のアカウントを取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkEnum」を参照してください](iolkenum.md)。
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>パラメーター

_ppunk_
  
> [in]クライアントが **IOlkAccount** インターフェイスを取得するためにクエリを実行できる [IUnknown](iolkaccount.md) インターフェイスへのポインター。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|S_FALSE  <br/> |列挙子が最後に達しました。  <br/> |
   
## <a name="remarks"></a>注釈

*ppunk で指定されたインターフェイスは***、IUnknown から継承します**。 クライアントは、このインターフェイスを **(IUnknown::QueryInterface** を使用して) クエリを実行して **、IOlkAccount** インターフェイスへのポインターを取得し、このアカウントの情報を取得または設定できます。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

