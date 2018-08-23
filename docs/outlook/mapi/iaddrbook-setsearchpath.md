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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571760"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
名前解決の処理に使用されるプロファイルに新しい検索パスを設定します。 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpSearchPath_
  
> [in]検索パスを保持するために使用する[SRowSet](srowset.md)構造体へのポインター。 **SRowSet**で**aRow**メンバーごとに、最初のプロパティは、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) である必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検索パスが正しく設定されました。
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> **PR_ENTRYID**プロパティは、 **SRowSet**構造で説明されているコンテナーの 1 つ含まれていません。 
    
## <a name="remarks"></a>注釈

クライアントとサービス ・ プロバイダーは、 [IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを使用して名前を解決するために使用されるコンテナーの検索順序に加えられた変更を保存する**SetSearchPath**メソッドを呼び出します。 検索パスは、セッションのインスタンス間で保存されます。 
  
クライアントとプロバイダーがありません、検索パスの変更を適用する[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[PidTagContainerFlags 標準プロパティ](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

