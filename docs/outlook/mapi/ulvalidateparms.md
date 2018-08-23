---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804166"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**適用対象**: Outlook 
  
パラメーターのクライアント アプリケーションが、サービス ・ プロバイダーおよび MAPI 経過をチェックする内部関数が呼び出されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT UlValidateParms(
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
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> エラーの操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

MAPI とサービスの間で渡されるパラメーターを正しくし、 [CheckParms](checkparms.md)マクロのデバッグ検証のみを行うプロバイダーと見なされます。 プロバイダーは、クライアント アプリケーションによって渡されるすべてのパラメーターを確認する必要がありますが、クライアントが MAPI およびプロバイダーのパラメーターが正しいことを想定する必要があります。 戻り値をテストするのにには、 **HR_FAILED**マクロを使用します。 
  
**UlValidateParms**マクロは、呼び出し元のコードが C または C++ のどちらであるかに応じて異なる方法で呼び出されます。 HRESULT 値の代わりに ULONG を返すいくつかの**IUnknown**と MAPI メソッドのパラメーターを検証するためにこのマクロを使用します。[ValidateParms](validateparms.md)マクロは、他のすべてのユーザーに対して機能します。 
  

