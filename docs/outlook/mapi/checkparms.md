---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5732dd3c1587c127cf153ebcadd9b791e6abb9ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582036"
---
# <a name="checkparms"></a>CheckParms

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI によって呼び出されるサービス プロバイダーのメソッドのデバッグ パラメーターを検証するために内部の関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _」方法_
  
> [in]確認する方法を列挙型を指定します。 
    
 _First/先頭のレコード_
  
> [in]スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

[ValidateParms](validateparms.md)と[UlValidateParms](ulvalidateparms.md)のマクロとは異なり、 **CheckParms**マクロでは、完全なパラメーターの検証は実行されません。 MAPI とサービスの間で渡されるパラメーター プロバイダーと見なされ、正しい**CheckParms**デバッグ検証のみを実行するようにします。 
  

