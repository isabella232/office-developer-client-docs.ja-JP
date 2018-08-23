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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800327"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**適用対象**: Outlook 
  
1 つまたは複数のエントリ、メッセージを通常のユーザーまたは配布リストにコピーします。
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpEntries_
  
> [in]コピーするエントリのエントリ id が含まれている[ENTRYLIST](entrylist.md)構造体の配列へのポインター。 
    
 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。 _UlFlags_パラメーターに AB_NO_DIALOG フラグが設定されている場合、 _ulUIParam_パラメーターは 0 にする必要があります。 
    
 _lpProgress_
  
> [in]進行状況インジケーターの場合、または NULL を表示する進行中のオブジェクトへのポインター。 _LpProgress_が NULL の場合は、 [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを介して、MAPI によって提供される進行中のオブジェクトを使用して進行状況のインジケーターを表示する必要があります。 _UlFlags_に AB_NO_DIALOG フラグが設定されている場合、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]コピー操作の実行方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
AB_NO_DIALOG 
  
> 進行状況インジケーターの表示を抑制します。 このフラグが設定されていない場合は、進行状況のインジケーターが表示されます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 緩やかなレベルの重複するエントリのチェックを実行することを示します。 緩やかな重複するエントリのチェックの実装は、特定のプロバイダーです。 などのプロバイダーは、同じ 2 つのエントリの表示名と緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 厳密なレベルの重複するエントリのチェックを実行することを示します。 厳密な重複するエントリのチェックの実装は、特定のプロバイダーです。 などのプロバイダーは、両方同じ 2 つのエントリの名前とメッセージのアドレスを表示すると、厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2 つ重複していることが判明した場合に新しいエントリが既存のものを置換する必要があることを示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> コピー操作が成功しました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> コピー操作は完了しましたが、1 つまたは複数のエントリをコピーできませんでした。 この値が返されると、呼び出しを成功として処理する必要があります。 この値をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IABContainer::CopyEntries**メソッドは、同じコンテナーまたは別のコンテナーからエントリをコピーします。 **CopyEntries**への呼び出しは、コピーするには、各エントリの次の呼び出しと同等の機能です。 
  
1. 新しいエントリを作成する[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドです。 
    
2. コピーするエントリからプロパティを読み取る[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドです。 
    
3. 新しいエントリのプロパティを記述する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。 
    
4. [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを新しいエントリの保存を実行します。 
    
5. コンテナーの参照を解放するのには、新しいエントリの[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)のメソッドです。 
    
## <a name="notes-to-implementers"></a>実装者へのメモ

**IABContainer::CopyEntries**メソッドをサポートするすべてのコンテナーは、変更可能である必要があります。 変更可能であることを示すには、その**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで、コンテナーの AB_MODIFIABLE フラグを設定します。 
  
すべてのフラグの操作をサポートする必要があります。ただし、解釈し、これらのフラグの使用は、特定の実装-は、実装のコンテキストでは、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグの意味は何を意味を判断できます。 できないかのエントリは、重複しているかどうかを決定できません、コピーするエントリを常に許可します。 
  
CREATE_REPLACE フラグが設定されている場合は、常に CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT を設定するかどうかと、エントリは、重複しているかどうかに関係なくエントリをコピーします。 
  
CREATE_REPLACE が設定されていない場合は、CREATE_CHECK_DUP_STRICT の設定は、重複データをチェックします。 重複エントリが確認された場合は、エントリをコピーできません。 
  
CREATE_REPLACE; をサポートする必要はありません。CREATE_REPLACE をサポートしていないことは、無視しても安全とコピーが常に実行を意味します。 
  
重複していないエントリをコピーできない場合にのみ、MAPI_W_PARTIAL_COMPLETION の警告を返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロバイダーに重複するエントリのチェックを実行するためにコンテナーをどのようにするかを示すために、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT フラグを使用します。 重複しているかどうかに関係なく追加のエントリがある場合は、いずれかまたは設定しませんこれらのフラグのいずれかの CREATE_REPLACE フラグを設定します。 CREATE_REPLACE は、エントリが重複の場合を限定しないことを示します常にそれをする元のエントリを置き換えます。 
  
## <a name="see-also"></a>関連項目



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

