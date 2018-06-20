---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800541"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo: IMAPIProp

  
  
**適用されます**: Outlook 
  
フォームの定義には特定のプロパティには、クライアント アプリケーション アクセスを提供します。 フォームの情報を保持する別のオブジェクトに、フォーム ライブラリのプロバイダーは、フォームをアクティブにすることがなくクライアントにフォームを記述できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |フォーム オブジェクトの情報  <br/> |
|によって実装されます。  <br/> |フォーム ライブラリのプロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormInfo  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMINFO  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |フォームを使用するプロパティの完全なセットへのポインターを返します。  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |フォームを使用する動詞の完全なセットへのポインターを返します。  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |フォームのアイコンのプロパティからアイコンを作成します。  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |構成ファイル内の特定のフォームの説明を保存します。  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |特定のフォームがインストールされているフォームのコンテナーへのポインターを返します。  <br/> |
   
## <a name="remarks"></a>備考

MapiForm.h ヘッダー ファイルで定義されているほとんどのインタ フェースとは異なり、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しを通じてほとんどのフォームの情報をエクスポートするため**IMAPIFormInfo**を[IMAPIProp](imapipropiunknown.md)インターフェイスから継承します。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

