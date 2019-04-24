---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349309"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決プロセスで使用されるプロファイルに新しい検索パスを設定します。 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpSearchPath_
  
> 順番検索パスを保持するために使用する[srowset](srowset.md)構造体へのポインター。 **srowset**の各**arow**メンバーの最初のプロパティは、 **** ([PidTagEntryId](pidtagentryid-canonical-property.md)) である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索パスが正常に設定されました。
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> **srowset**構造で記述されているコンテナーの1つに、 **PR_ENTRYID**プロパティが含まれていませんでした。 
    
## <a name="remarks"></a>解説

クライアントおよびサービスプロバイダーは、 **SetSearchPath**メソッドを呼び出して、 [IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドを使用して名前を解決するために使用されるコンテナー検索順序に加えられた変更を保存します。 検索パスは、セッションのインスタンス間で保存されます。 
  
クライアントとプロバイダーは、検索パスを永続的に変更するために、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要はありません。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

