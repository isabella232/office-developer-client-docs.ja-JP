---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348371"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存の表の先頭に列を追加または移動します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>パラメーター

 _lptbl_
  
> 順番影響を受ける MAPI テーブルへのポインター。 
    
 _lpproptagColumnsNew_
  
> 順番表の先頭に追加または移動するプロパティのプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpfnFilterColumns_
  
> 順番呼び出し元によって送信されたコールバック関数へのポインター。 _lpfnFilterColumns_パラメーターが NULL に設定されている場合は、コールバックは行われません。 
    
 _ptaga_
  
> 順番プロパティを追加または先頭に移動する前に、テーブルに既に存在しているプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 **hraddcolumnsex**は、 _lpfnFilterColumns_によって参照されるコールバック関数へのパラメーターとしてこのポインターを渡します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、指定された列が移動または追加されました。
    
## <a name="remarks"></a>解説

_lpproptagColumnsNew_パラメーターを使用して**hraddcolumnsex**に渡されたプロパティは、次に[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出したときに公開される最初のプロパティになります。 _lpproptagColumnsNew_パラメーターで指定されていないテーブル内のプロパティはすべて、追加されて移動されたプロパティの後に公開されます。 
  
**QueryRows**が呼び出されたときにテーブルのプロパティが未定義の場合は、プロパティの種類 PT_NULL およびプロパティ識別子 PROP_ID_NULL を使用して返されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**hraddcolumnsex**関数を使用すると、呼び出し元は、テーブル内に既に存在している列をフィルター処理するためのコールバック関数を与えることができます。たとえば、文字列をプロパティ型 PT_UNICODE から PT_STRING8 に変換します。 **hraddcolumnsex**は、コールバック関数へのパラメーターとして既に存在する列セットへのポインターを渡します。 コールバック関数は、property タグ配列内のデータを変更できますが、新しいタグを追加することはできません。 
  
 **hraddcolumnsex**は、最初にコールバック関数を呼び出し、次に、指定された列を追加または移動して、最後に[IMAPITable:: SetColumns](imapitable-setcolumns.md)を呼び出します。 
  
_lpAllocateBuffer_および_lpfreebuffer_入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIFreeBuffer](mapifreebuffer.md)関数をポイントします。 **hraddcolumnsex**に渡されるポインターの正確な値は、呼び出し元がクライアントアプリケーションであるかサービスプロバイダーであるかによって異なります。 クライアントは、指定された名前を持つ MAPI 関数へのポインターを渡します。 サービスプロバイダーは、初期化呼び出しで受け取ったポインターまたは[imapisupport:: getmemallocroutines](imapisupport-getmemallocroutines.md)メソッドを呼び出して取得したポインターを渡します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

