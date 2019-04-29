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
  
テーブルにフィルターを適用し、指定された条件に一致する行だけを行のセットに絞ります。
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpRestriction_
  
> 順番フィルターの条件を定義する[srestriction](srestriction.md)構造体へのポインター。 _lpRestriction_パラメーターで NULL を渡すと、現在のフィルターが削除されます。 
    
 _ulFlags_
  
> 順番制限操作のタイミングを制御するフラグのビットマスク。 次のフラグを設定できます。
    
TBL_ASYNC 
  
> 操作を非同期的に開始し、操作が完了する前に制御を戻します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまで、フィルターの評価を延期します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フィルターが正常に適用されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中のため、制限操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_TOO_COMPLEX 
  
> _lpRestriction_パラメーターによって参照される特定のフィルターが複雑すぎるため、テーブルが操作を実行できません。 
    
## <a name="remarks"></a>注釈

**IMAPITable:: Restrict**メソッドは、テーブルに制限またはフィルターを設定します。 以前の制限がある場合は、破棄され、新しい適用が適用されます。 制限を適用しても、テーブルの基になるデータには影響しません。単に、制限を満たすデータを含む行に取得できる行を制限することで、ビューを変更します。 
  
いくつかの異なる種類の制限があり、それぞれ異なる構造で記述されています。 [srestriction](srestriction.md)構造体には、制限の種類を示す値と、その型に適用できる特定の構造を示す2つのメンバーが含まれています。 
  
**制限**の呼び出しによって非表示にされたテーブルの行に対する通知は生成されません。 
  
複数値プロパティのプロパティ制限は、単一値プロパティの制限のように動作します。 プロパティ制限で使用される複数値プロパティには、MVI_FLAG フラグが設定されている必要があります。 このフラグが設定されていない場合は、完全に順序付けられた組として扱われます。 2つの複数値の列の比較では、列の要素が順番に比較され、最初の不等式の列のリレーションシップがレポートされます。 等式が返されるのは、列の比較結果が同じ順序で同じ値を含む場合だけです。 一方の列の値がもう一方の列の値よりも小さい場合は、レポートされたリレーションシップは、null 値が他の値になることを示します。
  
制限の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。
  
> [!NOTE]
> サーバー上のデータを検索する動的なクエリを作成する場合は、 **Restrict**メソッドと**QueryRows**メソッドを一緒に使用するのではなく、 **FindRow**メソッドを使用します。 **Restrict**メソッドは、ベースフォルダーに追加または変更されたすべてのメッセージを評価するために使用されるキャッシュビューを作成します。 クライアントアプリケーションが各動的クエリに対して**Restrict**メソッドを使用する場合は、クエリごとにキャッシュされたビューが作成されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

現在の制限を新しいものを作成せずに破棄するには、 _lpRestriction_で NULL を渡します。
  
別の非同期テーブル呼び出しが進行中で、 **Restrict**が MAPI_E_BUSY を返す原因となっている場合は、 [IMAPITable:: Abort](imapitable-abort.md)を呼び出して、呼び出しを停止することができます。 
  
 **** フラグの1つを設定しない限り、操作を同期することはできません。 TBL_BATCH フラグを設定した場合**** 、データを要求しない限り、制限の評価は延期されます。 TBL_ASYNC フラグが設定されている場合、動作を非同期に**制限**し、操作が完了する前に戻る可能性があります。
  
**Restrict**の呼び出しが行われ、BOOKMARK_CURRENT がテーブルの先頭に設定されている場合、テーブルのすべてのブックマークは破棄されます。 
  
テーブルの列セットに含まれていないプロパティにプロパティ制限を設定しようとすると、結果は未定義となります。 プロパティがテーブルでサポートされているかどうかがわからない場合は、プロパティ制限と exists 制限を組み合わせて使用します。 exists 制限は、プロパティの制限を課す前に、プロパティが存在するかどうかを確認します。 
  
制限のためにテーブルからフィルター処理された行に対してテーブル通知を受信することは予想されません。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl:: applyrestriction  <br/> |mfcmapi は、 **IMAPITable:: Restrict**メソッドを使用して、テーブルに制限を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

