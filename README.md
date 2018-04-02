# CsDotPic3DAry
三次元配列を使って複数のドット絵表示（.NET Core）

## 処理
三次元配列のデータを`foreach`文を使って出力する。

## コード
```
using System;

namespace Dotary3d
{
    class Dotary3d
    {
        static void Main(string[] args)
        {
            int[][][] letters =
            {
                new int[][] 
                { 
                    new int[] {0, 0, 1, 1, 0, 0},
                    new int[] {0, 1, 0, 0, 1, 0},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 1, 1, 1, 1, 1},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 0, 0, 0, 0, 1}
                },
                new int[][]
                {
                    new int[] {1, 1, 1, 1, 1, 0},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 1, 1, 1, 1, 0},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 1, 1, 1, 1, 0}
                },
                new int[][]
                {
                    new int[] {0, 1, 1, 1, 1, 0},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {1, 0, 0, 0, 0, 0},
                    new int[] {1, 0, 0, 0, 0, 0},
                    new int[] {1, 0, 0, 0, 0, 1},
                    new int[] {0, 1, 1, 1, 1, 0}
                }
            };

            foreach (int[][] img in letters)
            {
                foreach (int[] line in img)
                {
                    foreach (int dot in line)
                    {
                        if (dot == 1)
                        {
                            Console.Write("#");
                        }
                        else
                        {
                            Console.Write(" ");
                        }
                    }
                    Console.WriteLine();
                }
                Console.WriteLine();
            }
        }
    }
}
```

## 出力結果  
```
  ##
 #  #
#    #
######
#    #
#    #

#####
#    #
#####
#    #
#    #
#####

 ####
#    #
#
#
#    #
 ####
```
  
## 開発環境
| 開発ツール |  |
|:-|:-|
| OS | Windows10 |
| 統合開発環境(IDE) | Visual Studio Community 2017 |
| 開発言語 | Visual C# |
