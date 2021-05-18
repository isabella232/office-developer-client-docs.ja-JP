---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: 列挙子の次のアカウントを取得します。
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405990"
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

