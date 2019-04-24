---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346397"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のエントリ (通常はメッセージングユーザーまたは配布リスト) をコピーします。
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpentries_
  
> 順番コピーするエントリのエントリ識別子を含む[entrylist](entrylist.md)構造体の配列へのポインター。 
    
 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 _ulflags_パラメーターに AB_NO_DIALOG フラグが設定されている場合、 _uluiparam_パラメーターは0である必要があります。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター、または NULL。 _lpprogress_が NULL の場合、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドによって、MAPI によって提供される progress オブジェクトを使用して進行状況インジケーターを表示する必要があります。 AB_NO_DIALOG フラグが_ulflags_で設定されている場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番コピー操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> 進行状況インジケーターの表示を抑制します。 このフラグが設定されていない場合は、進行状況のインジケーターが表示されます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 重複したエントリのチェックを緩やかに実行する必要があることを示します。 重複していない重複するエントリのチェックは、プロバイダーに固有のものです。 たとえば、プロバイダーは、同じ表示名を持つ2つのエントリとして緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 重複するエントリの厳密なチェックを実行する必要があることを示します。 厳密に重複したエントリチェックの実装は、プロバイダーに固有のものです。 たとえば、プロバイダーは、同じ表示名とメッセージアドレスの両方を持つ2つのエントリとして厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2つのレコードが重複していると判断された場合は、新しいエントリで既存のエントリを置き換える必要があることを示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コピー操作が正常に完了しました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 全体のコピー操作に成功しましたが、1つ以上のエントリをコピーできませんでした。 この値が返されると、呼び出しが成功したとして処理されます。 この値をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**IABContainer:: copyentries**メソッドは、同じコンテナーまたは別のコンテナーからエントリをコピーします。 **copyentries**の呼び出しは、各エントリのコピーに対して次の呼び出しを行うことと機能的には同じです。 
  
1. [IABContainer:: createentry](iabcontainer-createentry.md)メソッドを実行して、新しいエントリを作成します。 
    
2. コピーするエントリからプロパティを読み取るための[imapiprop:: GetProps](imapiprop-getprops.md)メソッド。 
    
3. [imapiprop:: setprops](imapiprop-setprops.md)メソッドを実行して、新しいエントリにプロパティを書き込みます。 
    
4. 保存を実行するための、新しいエントリの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッド。 
    
5. コンテナーの参照を解放するための、新しいエントリの[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッド。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**IABContainer:: copyentries**メソッドをサポートするすべてのコンテナーを変更可能にする必要があります。 コンテナーの AB_MODIFIABLE フラグを**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、それが変更可能であることを示します。 
  
すべてのフラグをサポートする必要があります。ただし、これらのフラグの解釈と使用は実装に固有です。つまり、実装のコンテキストで CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグの意味を判断できます。 エントリが重複しているかどうかを判断できない場合、または指定しない場合は、常にエントリのコピーが許可されます。 
  
CREATE_REPLACE フラグが設定されている場合は、CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT が設定されているかどうかと、エントリが重複しているかどうかに関係なく、常にエントリをコピーします。 
  
CREATE_REPLACE が設定されておらず、CREATE_CHECK_DUP_STRICT が設定されている場合は、重複をチェックします。 エントリが重複していると判断された場合は、エントリをコピーしないでください。 
  
CREATE_REPLACE をサポートする必要はありません。CREATE_REPLACE をサポートしていない場合は、無視して安全にコピーを実行できることを意味します。 
  
重複していないエントリをコピーできない場合にのみ、警告 MAPI_W_PARTIAL_COMPLETION を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

CREATE_CHECK_DUP_LOOSE および CREATE_CHECK_DUP_STRICT フラグを使用して、コンテナーが複製入力チェックを実行する方法をプロバイダーに示します。 重複しているかどうかにかかわらずエントリを追加する必要がある場合は、これらのフラグのどちらも設定しないか、CREATE_REPLACE フラグを設定します。 CREATE_REPLACE は、エントリが重複していてもかまわないことを示します。常に、元のエントリを置換することをお勧めします。 
  
## <a name="see-also"></a>関連項目



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

