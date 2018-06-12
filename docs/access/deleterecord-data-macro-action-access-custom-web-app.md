---
title: 関係するデータ マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: DeleteRecord/レコードの削除アクションを使用して、レコードを削除できます。
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798535"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>関係するデータ マクロのアクション (カスタム web アプリケーションのアクセス)

" **DeleteRecord/レコードの削除** " アクションを使用して、レコードを削除できます。 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**DeleteRecord** アクションの引数は次のとおりです。 
  
|**引数**|**説明**|
|:-----|:-----|
|**レコードの別名** <br/> |削除するレコードを識別する文字列です。 *別名*引数を指定しない場合は、現在のレコードが削除されます。  <br/> |
   
## <a name="remarks"></a>解釈

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。 
  
`[LastCreateRecordIdentity]`


