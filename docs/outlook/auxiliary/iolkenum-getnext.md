---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: 列挙子では、次のアカウントを取得します。
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799507"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

列挙子では、次のアカウントを取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkEnum](iolkenum.md)を参照してください。
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>パラメーター

_ppunk_
  
> [in][IOlkAccount](iolkaccount.md)インターフェイスを取得するのには、クライアントが照会できる**IUnknown**インターフェイスへのポインター。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|S_FALSE  <br/> |列挙子には、末尾に到達します。  <br/> |
   
## <a name="remarks"></a>注釈

*Ppunk*によって指定されたインターフェイスは、 **IUnknown**から継承します。 クライアントは、 **IOlkAccount**インターフェイスへのポインターを取得する ( **IUnknown::QueryInterface**を使用して) このインターフェイスを問い合わせることができますを取得したり、このアカウントの情報を設定します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

