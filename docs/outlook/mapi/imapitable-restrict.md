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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800855"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**適用対象**: Outlook 
  
指定した条件に一致する行のみに設定した行を減らすこと、テーブルにフィルターを適用します。
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> [in][SRestriction](srestriction.md)フィルターの条件を定義する構造体へのポインター。 _LpRestriction_パラメーターに NULL を渡すと、現在のフィルターが削除されます。 
    
 _ulFlags_
  
> [in]制限操作のタイミングを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TBL_ASYNC 
  
> 操作を非同期に開始し、操作が完了する前に返します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまでは、フィルターの評価を延期します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フィルターが正常に適用されました。
    
MAPI_E_BUSY 
  
> 別の操作では、制限操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_TOO_COMPLEX 
  
> テーブルは、 _lpRestriction_パラメーターで指定された特定のフィルターが複雑すぎるために、操作を実行できません。 
    
## <a name="remarks"></a>注釈

**IMAPITable::Restrict**メソッドは、制限、またはテーブル上のフィルターを設定します。 以前の制限がある場合は、それは破棄され、新しいものが適用されます。 制限を適用するのには影響しません、テーブルの基になるデータだけで、制限を満たすデータを含む行を取得できる行数を制限することによってビューを変更します。 
  
さまざまな種類の制限、構造が異なると、それぞれについて説明します。 [SRestriction](srestriction.md)構造には、2 つのメンバーが含まれています: を制限し、そのタイプに該当する特定の構造の種類を示す値です。 
  
ビューから非表示に**制限**を呼び出すことによってテーブルの行の通知が生成されることはありません。 
  
複数値を持つプロパティのプロパティの制限は、単一値を持つプロパティに対する制限と同じように動作します。 プロパティ制限で使用する複数値を持つプロパティには、MVI_FLAG フラグが設定されている必要があります。 このフラグが設定されていない場合、は、完全に順序付けられた組として扱われます。 2 つの複数値を持つ列の比較では、最初の非等値の列の関係をレポートの列の要素を比較します。 比較の列に同じ順序で同じ値が含まれている場合にのみ、等しいかどうかが返されます。 もう一方よりも少ない値を 1 つの列には、報告された関係が他の値に null 値の
  
制限の詳細については、[制限の詳細](about-restrictions.md)を参照してください。
  
> [!NOTE]
> サーバー上のデータを検索する動的なクエリを作成する場合は、 **Restrict**メソッドおよび**スプーラー**メソッドを共に使用するのではなく**FindRow**メソッドを使用します。 **Restrict**メソッドでは、すべてのメッセージでは、ベースのフォルダーを追加または変更を評価するために使用されるキャッシュされたビューを作成します。 クライアント アプリケーションは、動的クエリごとに、 **Restrict**メソッドを使用する場合、キャッシュされたビューはクエリごとに作成されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

新規に作成することがなく、現在の制限を破棄するには、 _lpRestriction_に NULL を渡します。
  
別のテーブルの非同期呼び出しが実行中である場合、MAPI_E_BUSY に戻るには、**制限**の原因で呼び出すことができます、呼び出しを停止するのには[IMAPITable::Abort](imapitable-abort.md) 。 
  
 フラグのいずれかを設定しない限り、**制限**は同期的に動作します。 TBL_BATCH フラグを設定する場合、**制限**は、データを要求する場合を除き、制限の評価を延期します。 TBL_ASYNC フラグが設定されている場合**だけに制限する**機能、非同期的に操作が完了する前に返す可能性があります。
  
**制限**への呼び出しが作成され、テーブルの先頭に BOOKMARK_CURRENT、現在のカーソル位置を設定すると、テーブルのすべてのブックマークは破棄されます。 
  
テーブルの列のセットに含まれていないプロパティのプロパティの制限を適用しようとした場合、結果は定義されていません。 使用しているテーブルのプロパティがサポートされているかどうかには、結合のプロパティ制限で、制限が存在します。 プロパティの制限を適用する前にプロパティが存在する制限の確認が存在します。 
  
制限があるため、テーブルのフィルターされた行をテーブル通知が受信されないようにします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI では、 **IMAPITable::Restrict**メソッドを使用して、テーブル上の制限を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

