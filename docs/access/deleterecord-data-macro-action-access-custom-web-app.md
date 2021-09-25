---
title: DeleteRecord Data Macro アクション (Access custom Web app)
manager: lindalu
ms.date: 09/05/2021
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
ms.openlocfilehash: 01d0cdeecd7c1401c274822736a3cd40a865db52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586433"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>DeleteRecord Data Macro アクション (Access custom Web app)

You can use the **DeleteRecord** action to delete a record. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**DeleteRecord** アクションの引数は次のとおりです。 
  
|**Arg1 と Arg2 の値**|**説明**|
|:-----|:-----|
|**Record Alias/レコードの別名** <br/> |削除するレコードを識別する文字列。 Alias 引数  *を指定*  しない場合は、現在のレコードが削除されます。  <br/> |
   
## <a name="remarks"></a>注釈

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。 
  
`[LastCreateRecordIdentity]`
