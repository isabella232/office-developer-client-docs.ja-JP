---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414621"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルにフィルターを適用し、指定した条件に一致する行にのみ行セットを減らします。
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> [in]フィルターの [条件を定義する SRestriction](srestriction.md) 構造体へのポインター。 _lpRestriction_ パラメーターに NULL を渡すと、現在のフィルターが削除されます。 
    
 _ulFlags_
  
> [in]制限操作のタイミングを制御するフラグのビットマスク。 次のフラグを設定できます。
    
TBL_ASYNC 
  
> 操作を非同期的に開始し、操作が完了する前に返します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまで、フィルターの評価を延期します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フィルターが正常に適用されました。
    
MAPI_E_BUSY 
  
> 制限操作の開始を妨げる別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_TOO_COMPLEX 
  
> _lpRestriction_ パラメーターが指す特定のフィルターが複雑すぎるため、テーブルで操作を実行できません。 
    
## <a name="remarks"></a>注釈

**IMAPITable::Restrict** メソッドは、テーブルに制限 (フィルター) を設定します。 以前の制限がある場合は破棄され、新しい制限が適用されます。 制限を適用すると、テーブルの基になるデータに影響はありません。取得できる行を、制限を満たすデータを含む行に制限することで、ビューを変更します。 
  
制限にはいくつかの種類があります。それぞれ異なる構造で説明されています。 [SRestriction 構造体には](srestriction.md)、制限の種類と、その型に適用可能な特定の構造を示す値の 2 つのメンバーが含まれる。 
  
Restrict の呼び出しによって表示から非表示にされたテーブル行 **の通知** は生成されません。 
  
複数値プロパティのプロパティ制限は、単一値プロパティの制限と同様に機能します。 プロパティ制限で使用する複数値プロパティには、プロパティ フラグが設定MVI_FLAG必要があります。 このフラグを設定しない場合は、完全に順序付けられたタプルとして扱います。 2 つの複数値列の比較では、列要素を順番に比較し、列の関係を最初の不等式で報告します。 等号は、比較される列に同じ値が同じ順序で含まれている場合にのみ返されます。 1 つの列の値が他の列よりも少ない場合、報告される関係は、もう一方の値に対する null 値の関係になります。
  
制限の詳細については、「制限について [」を参照してください](about-restrictions.md)。
  
> [!NOTE]
> サーバー上のデータを検索する動的クエリを作成する場合は **、Restrict** メソッドと **QueryRows** メソッドを一緒に使用する代わりに **FindRow** メソッドを使用します。 **Restrict メソッド** は、ベース フォルダーに追加または変更されたメッセージを評価するために使用されるキャッシュ ビューを作成します。 クライアント アプリケーションが動的クエリごとに **Restrict** メソッドを使用する場合は、クエリごとにキャッシュ ビューが作成されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

新しい制限を作成せずに現在の制限を破棄するには  _、lpRestriction で NULL を渡します_。
  
別の非同期テーブル呼び出しが進行中で、Restrict が MAPI_E_BUSY を返す場合は[、IMAPITable::Abort](imapitable-abort.md)を呼び出して呼び出しを停止できます。 
  
 **Restrict** は、フラグのいずれかを設定しない限り、同期的に動作します。 [制限] フラグをTBL_BATCH **場合** は、データを要求しない限り、制限の評価が延期されます。 このフラグTBL_ASYNC設定されている場合 **、Restrict** は非同期的に動作し、操作が完了する前に戻る可能性があります。
  
テーブルのすべてのブックマークは **、Restrict** の呼び出しが行われたときに破棄され、現在のカーソル位置である BOOKMARK_CURRENT がテーブルの先頭に設定されます。 
  
テーブルの列セットに含めされていないプロパティにプロパティ制限を適用しようとすると、結果は未定義になります。 プロパティがテーブルでサポートされるかどうかが不明な場合は、プロパティ制限と存在する制限を組み合わせます。 存在する制限は、プロパティ制限を適用する前に、プロパティの存在をチェックします。 
  
制限のためにテーブルからフィルター処理された行に対するテーブル通知を受け取る必要はありません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI は **IMAPITable::Restrict** メソッドを使用して、テーブルに制限を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

