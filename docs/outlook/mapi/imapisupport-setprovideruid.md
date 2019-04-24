---
title: imapisupportsetprovideruid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326314"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーを一意に表す[MAPIUID](mapiuid.md)構造体を登録します。 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpproviderid_
  
> 順番アドレス帳またはメッセージストアプロバイダーを識別する**MAPIUID**構造体へのポインター。 
    
 _ulFlags_
  
> 予約語0である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> **MAPIUID**構造が正常に登録されました。 
    
## <a name="remarks"></a>解説

**imapisupport:: setprovideruid**メソッドは、アドレス帳とメッセージストアプロバイダーのサポートオブジェクトに実装されています。 これらのプロバイダーは、 **setprovideruid**を呼び出して、 _lpproviderid_によって参照されている**MAPIUID**構造体で記述された一意の識別子を登録します。 プロバイダーには、作成するすべてのエントリ識別子にこの識別子が含まれています。 
  
mapi は、 **MAPIUID**構造を使用して mapi スプーラーに送信メッセージを送信し、クライアント要求を処理するための適切なプロバイダーを決定します。 たとえば、クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出すと、MAPI はエントリ識別子の**MAPIUID**部分を調べ、それを**setprovideruid**に渡されたプロバイダーにマップし、そのプロバイダーの**openentry**を呼び出します。. 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIUID**構造を登録するには、ログオン時に**setprovideruid**を呼び出します。 MAPI では、アドレス帳とメッセージストアプロバイダーが複数の識別子を登録できます。 **setprovideruid**に対して複数の呼び出しを行うと、 **MAPIUID**が重複している場合でも、プロバイダーの**MAPIUID**構造のセットには常に**MAPIUID**構造が追加されます。 **setprovideruid**は**MAPIUID**を削除できません。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

