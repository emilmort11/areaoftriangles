# -*- coding: utf-8 -*-

import math


def distance(a, b):
    
    xa = a[0]
    ya = a[1]
    
    xb = b[0]
    yb = b[1]
    
    diff_x_sq = (xa - xb) ** 2
    diff_y_sq = (ya - yb) ** 2
    
    return math.sqrt(diff_x_sq + diff_y_sq)


def cacl_area_op_triangel(point1,point2,point3):
    a = distance(point1,point2)
    b = distance(point1,point3)
    c = distance(point2,point3)
    
    s = (a+b+c)/2
    
    a = s-a
    b = s-b
    c = s-c
    
    area = math.sqrt(s*a*b*c)
    
    print("area of triangel:" + str(area))
    
    return area
    
    
def split_line(content):
    
    points_strings = content.split(';')
    
    res = []
    
    for ps in points_strings:
        
        numbers_strings = ps.split(',')
        
        numbers = []
        for ns in numbers_strings:
            number = float(ns.strip())
            numbers.append(number)
        
        res.append(numbers)
        
    return res


if __name__ == '__main__':

    f = open('data/triangles.txt')
    
    triangles = []
    
    for line in f:
        
        content = line.strip()
        
        if content == '':
            print('Empty line detected')
            continue
        
        tr = split_line(content)
        triangles.append(tr)
    
    f.close()
    area = 0
    for tr in triangles:
        
        area = area + cacl_area_op_triangel(tr[0],tr[1],tr[2])
       
    print("Total area: " + str(round(area)))
