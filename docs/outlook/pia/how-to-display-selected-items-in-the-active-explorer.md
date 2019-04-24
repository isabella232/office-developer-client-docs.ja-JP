---
title: アクティブ エクスプローラーで選択した項目を表示する
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356386"
---
# <a name="display-selected-items-in-the-active-explorer"></a>アクティブ エクスプローラーで選択した項目を表示する

この例では、OutlookItem ヘルパー クラスを利用して、アクティブなエクスプローラー ウィンドウで選択したすべてのアイテムを簡単に表示する方法を示しています。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) オブジェクトには、アクティブな Outlook エクスプローラーで現在選択されている Outlook アイテムのセットが含まれています。 [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)) で表されるアクティブなエクスプローラーも、選択されたアイテムのセットも、選択されているアイテムの種類を示しません。 通常、最初にアイテムの種類を識別して、その種類に応じた固有の **Display** メソッドを呼び出す必要があります。 **Display** メソッドはすべての Outlook アイテム オブジェクトに共通していて、このメソッドは OutlookItem ヘルパー クラスに含まれているため、このヘルパー クラスを利用して、OutlookItem オブジェクトのインスタンスである myItem を宣言すると、myItem.Display を使用して選択された各アイテムを表示できます。 OutlookItem ヘルパー クラスの実装方法は、「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」を参照してください。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a>関連項目

- [ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Outlook アイテム全般](general-outlook-items.md)

