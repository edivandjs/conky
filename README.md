# conky
My conky

# Conky, a system monitor, based on torsmo
background no
use_xft yes
font Dejavu Sans:size=8
xftalpha 0
update_interval 2.0
total_run_times 0
own_window yes
own_window_transparent yes
#own_window_type desktop
own_window_hints undecorated,below,skip_taskbar,sticky
own_window_argb_visual yes
own_window_argb_value 150
own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager
double_buffer yes
minimum_size 235 235
maximum_width 280
draw_shades no
draw_outline yes
draw_borders no
draw_graph_borders no
default_color 999999
default_shade_color black
default_outline_color black
alignment top_right
gap_x 8
gap_y 123
no_buffers yes
cpu_avg_samples 2
text_buffer_size 1024
override_utf8_locale no
uppercase no
double_buffer yes
TEXT
S I S T E M A
$hr
Sistema: $sysname $kernel
${color grey}Tempo escedido:$color $uptime
Hora: ${time %H:%M:%S} Data: ${time %e/%b/13}
C P U$alignr ${cpu cpu0}%
$hr
Procesador: ${alignr}${freq_g}GHz / 2.28GHz
grep @ /proc/cpuinfo
${color green}${cpubar 4 cpu0}${color grey}
${color green}${cpubar 4 cpu1}${color grey}
${color green}${cpubar 4 cpu2}${color grey}
${color green}${cpubar 4 cpu3}${color grey}
${color green}${cpubar 4 cpu4}${color grey}
${color green}${cpubar 4 cpu5}${color grey}
${color green}${cpubar 4 cpu6}${color grey}
${color green}${cpubar 4 cpu7}${color grey}
T O P C P U
$hr
Proceso$alignr CPU% MEM%
${top name 1}$alignr${top cpu 1} ${top mem 1}
${top name 2}$alignr${top cpu 2} ${top mem 2}
${top name 3}$alignr${top cpu 3} ${top mem 3}

R A M$alignr $memperc%
$hr
Memoria: ${alignr}${mem} / ${memmax}
${color green}${membar 4}${color grey}
T O P R A M
$hr
Proceso $alignr CPU% MEM%
${top_mem name 1}$alignr${top_mem cpu 1} ${top_mem mem 1}
${top_mem name 2}$alignr${top_mem cpu 2} ${top_mem mem 2}
${top_mem name 3}$alignr${top_mem cpu 3} ${top_mem mem 3}

A R M A Z E N A M E N T O
$hr
Raiz: ${alignr}$color${fs_used /} / ${fs_size /}
${color green}${fs_bar 4 /}${color grey}
Home: ${alignr}$color${fs_used /home} / ${fs_size /home}
${color green}${fs_bar 4 /home}${color grey}
${alignr}$color${fs_used /run/media/edivan/HDD Samsung} 
${fs_size /run/media/edivan/HDD Samsung}
${color green}${fs_bar 4 /run/media/edivan/SSD Backup}${color grey}
R E D E S${alignr}${downspeed eth0}
${color green}REDE ${hr 1}${color}
Eth0 ${alignr}IP: ${addr enp4s0}
Down ${downspeed eth0} k/s ${alignr}Up ${upspeed eth0} k/s
${downspeedgraph enp4s0 } ${alignr}${upspeedgraph enp4s0 }
Total ${totaldown eth0} ${alignr}Total
Entrada/Saida ${alignr}${totaldown enp4s0} / ${totalup enp4s0}
