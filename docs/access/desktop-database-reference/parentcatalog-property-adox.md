---
title: ParentCatalog プロパティ (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603414"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog プロパティ (ADOX)


**適用されます**Access 2013 |。Office 2013

プロバイダー固有のプロパティへのアクセスを提供する、テーブルまたは列の親カタログを指定します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[Catalog](catalog-object-adox.md) オブジェクトを設定および取得します。 **ParentCatalog** を開かれた **Catalog** に設定すると、テーブルまたは列を **Catalog** コレクションに追加する前に、プロバイダー固有のプロパティにアクセスできます。

## <a name="remarks"></a>解説

データ プロバイダーの中には、作成時 (テーブルまたは列が **Catalog** コレクションに追加されるとき) のみプロバイダー固有のプロパティ値を設定できるものがあります。 **Catalog** にオブジェクトを追加する前に、これらのプロパティにアクセスするには、あらかじめ **ParentCatalog** プロパティで **Catalog** を指定しておきます。

テーブルまたは列を **ParentCatalog** 以外の **Catalog** に追加すると、エラーが発生します。

