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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426206"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前解決プロセスに使用するプロファイル内の新しい検索パスを設定します。 
  
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
  
> [in]検索パスを保持するために使用される [SRowSet](srowset.md) 構造体へのポインター。 **SRowSet** の **各 aRow** メンバーの最初のプロパティは、PR_ENTRYID **(** [PidTagEntryId) である必要があります](pidtagentryid-canonical-property.md)。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索パスが正常に設定されました。
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> **SRowSet** 構造体で説明されているコンテナーの 1 つには、その **プロパティPR_ENTRYID含** めなかった。 
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **、SetSearchPath** メソッドを呼び出して [、IAddrBook::ResolveName](iaddrbook-resolvename.md) メソッドで名前を解決するために使用されるコンテナー検索順序に加えた変更を保存します。 検索パスは、セッションのインスタンス間で保存されます。 
  
クライアントとプロバイダーは、検索パスの変更を永続的に行うために [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

