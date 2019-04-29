---
title: imapisupportmodifyprofile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419990"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロファイルセクションの変更を永続的に行います。
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番メッセージストアの種類を示すフラグのビットマスク。 次のフラグを設定できます。
    
MDB_TEMPORARY 
  
> メッセージストアは一時的なものであり、メッセージストアテーブルに追加することはできません。 MDB_TEMPORARY が設定されている場合、 **modifyprofile**はすぐに S_OK を返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルセクションの変更が成功しました。
    
## <a name="remarks"></a>注釈

**imapisupport:: modifyprofile**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対して実装されています。 メッセージストアプロバイダーは、「 **modifyprofile** 」を呼び出して、プロファイル情報の変更を MAPI に要求します。 
  
 **modifyprofile**は、呼び出し元プロバイダーに関連付けられているプロファイルセクションを、インストール済みのメッセージストアプロバイダーリソースの一覧に追加します。 これにより、メッセージストアがメッセージストアテーブルにリストされます。これは、クライアントが[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メソッドを使用して利用でき、ダイアログボックスを表示せずに開くことができます。 
  
MDB_TEMPORARY フラグが設定されている場合、MAPI は nothing を返し、メソッドはすぐに S_OK で戻ります。
  
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

