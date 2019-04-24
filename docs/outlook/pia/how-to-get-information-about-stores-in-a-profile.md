---
title: プロファイルのストアに関する情報を取得する
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2044fc52370bdadd5c7f01debbd02c88dd881715
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349421"
---
# <a name="get-information-about-stores-in-a-profile"></a>プロファイルのストアに関する情報を取得する

この例では、プロファイル内のストアを取得して列挙する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) コレクションを使用して、特定のプロファイルのストアを列挙できます。 **Stores** コレクションは、各 [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) オブジェクトに関する情報 (現在のプロファイルで **Store** オブジェクトがいつ追加されたか、 **Store** オブジェクトがいつ削除されるか、など) を公開するメンバーを提供します。 次のコード例の EnumerateStores は、現在のプロファイル内のストアを表す **Stores** オブジェクトを取得し、ストアを列挙します。 EnumerateStores は、**Stores** コレクション内の各 **Store** オブジェクトを調べます。 [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) プロパティの値が **true** (.pst または .ost ストアであることを示す) の場合は、 [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) プロパティと [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) プロパティが [ Listeners ](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに出力されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [ストア](stores.md)

